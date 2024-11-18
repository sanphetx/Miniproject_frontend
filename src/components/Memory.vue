<template>
  <div>
    <v-card>
      <v-card-title class="fade-enter-active fade-leave-active">แชร์เรื่องราว.....เรื่องราวดีๆเริ่มต้นจากตัวคุณแม่</v-card-title>
      <v-card-text>
        <v-list>
          <transition-group name="fade" tag="div">
            <v-card class="feed-card" v-for="(feed, index) in paginatedFeeds" :key="feed.id">
              <v-list-item>
                <v-list-item-content>
                  <v-list-item-title>ลำดับ {{ feed.index }}: {{ feed.feedname }}</v-list-item-title>
                  <v-list-item-subtitle>ชื่อผู้ใช้งาน: {{ feed.username }}</v-list-item-subtitle>
                  <v-list-item-subtitle>เนื้อหา:{{ feed.feedcontent }}</v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-action></v-list-item-action>
              </v-list-item>
            </v-card>
          </transition-group>
        </v-list>
      </v-card-text>
    </v-card>

    <v-card class="card-with-border">
      <v-card-title class="fade-enter-active fade-leave-active">ความทรงจำ</v-card-title>
      <v-card-text>
        <v-form @submit.prevent="addFeed">
          <v-text-field v-model="feedname" label="ชื่อหัวข้อ" required></v-text-field>
          <v-text-field v-model="username" label="ชื่อผู้ใช้" required></v-text-field>
          <v-text-field v-model="feedcontent" label="เนื้อหา" required></v-text-field>
          <v-btn color="primary" type="submit">เพิ่มความทรงจำ</v-btn>
        </v-form>
      </v-card-text>
    </v-card>

    <v-snackbar v-model="showSnackbar" :timeout="3000" color="error">
      {{ snackbarMessage }}
    </v-snackbar>

    <v-pagination
      v-model="currentPage"
      :length="totalPages"
      @input="paginateFeed"
    ></v-pagination>
  </div>
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
          this.feeds = response.data.reverse().map((feed, index) => {
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

<style>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}

.feed-card {
  border: 1px solid #ccc;
  border-radius: 5px;
  margin: 10px 0;
  padding: 10px;
}

.card-with-border {
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 15px;
}

.card-with-border.animated {
  transform: scale(1.1);
}
</style>
