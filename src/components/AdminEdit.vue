<template>
    <v-container fluid>
      <h2 class="text-center">Feeds</h2>
      <v-text-field
        v-model="searchUsername"
        label="ค้นหาด้วยชื่อผู้ใช้"
        outlined
        @input="searchFeeds"
      ></v-text-field>
  
      <v-dialog v-model="editingFeedDialog" max-width="600">
        <v-card>
          <v-card-title class="headline">{{ editingFeed ? 'Edit Feed' : 'Add Feed' }}</v-card-title>
          <v-card-text>
            <v-form @submit.prevent="editingFeed ? saveEditedFeed() : addFeed()">
              <v-text-field v-model="editedFeed.username" label="Username" required></v-text-field>
              <v-text-field v-model="editedFeed.feedname" label="Feed Name" required></v-text-field>
              <v-text-field v-model="editedFeed.feedcontent" label="Feed Content" required></v-text-field>
              <v-btn color="primary" type="submit">{{ editingFeed ? 'Save' : 'Add' }}</v-btn>
              <v-btn @click="cancelEdit">Cancel</v-btn>
            </v-form>
          </v-card-text>
        </v-card>
      </v-dialog>
  
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
              <v-btn @click="editFeed(feed)">Edit</v-btn>
              <v-btn @click="deleteFeed(feed)">Delete</v-btn>
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
  import axios from 'axios';
  
  export default {
    data() {
      return {
        feeds: [],
        username: '',
        feedname: '',
        feedcontent: '',
        editingFeed: null,
        editedFeed: {
          username: '',
          feedname: '',
          feedcontent: '',
        },
        editingFeedDialog: false,
        showSnackbar: false,
        snackbarMessage: '',
        currentPage: 1,   
        itemsPerPage: 5,  
        totalPages: 0,    
      };
    },
    methods: {
      fetchFeeds() {
        axios.get('http://localhost:9000/api/feeds')
          .then(response => {
            this.feeds = response.data.map((feed, index) => {
              feed.index = index + 1;
              return feed;
            });
  
            this.totalPages = Math.ceil(this.feeds.length / this.itemsPerPage);
          })
          .catch(error => {
            console.error('เกิดข้อผิดพลาดในการดึง Feed:', error);
          });
      },
      addFeed() {
        if (this.username.trim() !== '' && this.feedname.trim() !== '' && this.feedcontent.trim() !== '') {
          const newFeed = {
            username: this.username,
            feedname: this.feedname,
            feedcontent: this.feedcontent,
          };
  
          axios.post('http://localhost:9000/api/feeds', newFeed)
            .then(response => {
              this.username = '';
              this.feedname = '';
              this.feedcontent = '';
              this.fetchFeeds();
            })
            .catch(error => {
              console.error('เกิดข้อผิดพลาดในการเพิ่ม Feed:', error);
            });
        } else {
          if (this.username.trim() === '' || this.feedname.trim() === '' || this.feedcontent.trim() === '') {
            this.snackbarMessage = 'กรุณาใส่ชื่อผู้ใช้, ชื่อหัวข้อ และเนื้อหา';
            this.showSnackbar = true;
          } else if (this.username.trim() === '') {
            this.snackbarMessage = 'กรุณาใส่ชื่อผู้ใช้';
            this.showSnackbar = true;
          } else if (this.feedname.trim() === '') {
            this.snackbarMessage = 'กรุณาใส่ชื่อหัวข้อ';
            this.showSnackbar = true;
          } else {
            this.snackbarMessage = 'กรุณาใส่เนื้อหา';
            this.showSnackbar = true;
          }
        }
      },
      editFeed(feed) {
        this.editingFeed = feed;
        this.editedFeed.username = feed.username;
        this.editedFeed.feedname = feed.feedname;
        this.editedFeed.feedcontent = feed.feedcontent;
        this.editingFeedDialog = true;
      },
      saveEditedFeed() {
        axios.put(`http://localhost:9000/api/feeds/${this.editingFeed.id}`, this.editedFeed)
          .then(response => {
            this.fetchFeeds();
            this.cancelEdit();
          })
          .catch(error => {
            console.error('เกิดข้อผิดพลาดในการบันทึกการแก้ไข:', error);
          });
      },
      cancelEdit() {
        this.editingFeedDialog = false;
        this.editedFeed.username = '';
        this.editedFeed.feedname = '';
        this.editedFeed.feedcontent = '';
      },
      deleteFeed(feed) {
        axios.delete(`http://localhost:9000/api/feeds/${feed.id}`)
          .then(() => {
            this.fetchFeeds();
          })
          .catch(error => {
            console.error('เกิดข้อผิดพลาดในการลบ Feed:', error);
          });
      },
      startCardAnimation() {
        const card = document.querySelector('.card-with-border');
        card.classList.add('animated');
      },
      stopCardAnimation() {
        const card = document.querySelector('.card-with-border');
        card.classList.remove('animated');
      },
      paginateFeed() {
        this.fetchFeeds();
      },
    },
    computed: {
      paginatedFeeds() {
        const startIndex = (this.currentPage - 1) * this.itemsPerPage;
        const endIndex = startIndex + this.itemsPerPage;
        return this.feeds.slice(startIndex, endIndex);
      },
    },
    
    mounted() {
      this.fetchFeeds();
    },
  };
  </script>