<template>
    <v-container fluid>
      <h2 class="text-center">Feeds</h2>
      <v-text-field
        v-model="searchUsername"
        label="ค้นหาด้วยชื่อผู้ใช้"
        outlined
        @input="searchFeeds"
      ></v-text-field>
  
      <v-row justify="center">
        <v-col cols="12" sm="8" md="6" lg="4" v-for="feed in paginatedFeeds" :key="feed.id">
          <v-card>
            <v-card-title class="text-h6">{{ feed.feedname }}</v-card-title>
            <v-card-text>
              <div>
                <div>ชื่อผู้ใช้: {{ feed.username }}</div>
                <div>ชื่อเรื่อง: {{ feed.feedname }}</div>
                <div>เนื้อหา: {{ feed.feedcontent }}</div>
              </div>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
  
      <v-row justify="center">
        <v-col cols="12">
          <v-pagination v-model="currentPage" :length="totalPages"></v-pagination>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    data() {
      return {
        feeds: [],
        searchUsername: "",
        currentPage: 1,
        itemsPerPage: 5,
      };
    },
    computed: {
      paginatedFeeds() {
        const start = (this.currentPage - 1) * this.itemsPerPage;
        const end = start + this.itemsPerPage;
        return this.filteredFeeds.slice(start, end);
      },
      filteredFeeds() {
        if (this.searchUsername) {
          return this.feeds.filter((feed) =>
            feed.username.toLowerCase().includes(this.searchUsername.toLowerCase())
          );
        } else {
          return this.feeds;
        }
      },
      totalPages() {
        return Math.ceil(this.filteredFeeds.length / this.itemsPerPage);
      },
    },
    mounted() {
      this.fetchFeeds();
    },
    methods: {
      async fetchFeeds() {
        try {
          const response = await fetch("http://localhost:9000/api/feeds");
          if (response.ok) {
            this.feeds = await response.json();
          }
        } catch (error) {
          console.error("เกิดข้อผิดพลาดในการดึงข้อมูล Feeds:", error);
        }
      },
      searchFeeds() {
        this.currentPage = 1;
      },
    },
  };
  </script>
  
  <style scoped>
  .text-center {
    text-align: center;
  }
  </style>
  