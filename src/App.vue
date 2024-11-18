<template>
  <v-app>
    <!-- App Bar -->
    <v-app-bar app :style="{ backgroundColor: navbarColor }">
      <v-container>
        <v-row align="center" justify="space-between">
          <v-toolbar-title class="white--text">Mother Box</v-toolbar-title>
          <v-spacer></v-spacer>
          <v-btn text @click="goToHome">หน้าหลัก</v-btn>
          <v-btn text @click="goToMemory">ภาพความทรงจำ</v-btn>
          <v-btn text @click="goToHistory">ประวัติของคุณแม่</v-btn>
          <v-btn text @click="goToAgeDp">พัฒนาการ</v-btn>
          <v-btn text @click="goToConduct">การปฎิบัติตน</v-btn>
          <v-btn text @click="goToInfant">การกระตุ้นทารก</v-btn>
          <v-btn class="admin-edit-button" text @click="openAdminEdit">Admin Edit</v-btn>

          <v-dialog v-model="adminEditDialog" max-width="400">
            <v-card>
              <v-card-title>Enter Access Code</v-card-title>
              <v-card-text>
                <v-text-field v-model="accessCode" label="Access Code"></v-text-field>
              </v-card-text>
              <v-card-actions>
                <v-btn text @click="closeAdminEditDialog">Cancel</v-btn>
                <v-btn color="purple" @click="goToAdminEdit">Enter</v-btn>
              </v-card-actions>
            </v-card>
          </v-dialog>
        </v-row>
      </v-container>
    </v-app-bar>

    <v-main>
      <transition name="page-expandX" mode="out-in">
        <router-view />
      </transition>
    </v-main>

   
    <v-snackbar v-model="showAlert" :color="alertColor" :multi-line="multiLine">
      <span>{{ alertMessage }}</span>
      <template v-if="multiLine">
        <span>{{ alertMessageLine2 }}</span>
      </template>
      <v-btn text @click="showAlert = false">Close</v-btn>
    </v-snackbar>

    
    <v-footer dark padless>
      <v-card class="flex" flat tile>
        <v-card-title class="teal">
          <strong class="subheading">Sanphet Saefang</strong>
          <v-spacer></v-spacer>
          
          <a href="https://www.facebook.com/SanphetEx/" target="_blank">
            <v-btn dark icon>
              <v-icon size="24px">mdi-facebook</v-icon>
            </v-btn>
          </a>
          <a href="https://github.com/sanphet6410210319" target="_blank">
            <v-btn dark icon>
              <v-icon size="24px">mdi-github</v-icon>
            </v-btn>
          </a>
          <a href="https://www.instagram.com/sanphet.x/" target="_blank">
            <v-btn dark icon>
              <v-icon size="24px">mdi-instagram</v-icon>
            </v-btn>
          </a>
          <a href="https://mail.google.com/mail/u/0/?hl=th&tf=cm&fs=1&to=poposchter07@gmail.com" target="_blank">
            <v-btn dark icon>
              <v-icon size="24px">mdi-gmail</v-icon>
            </v-btn>
          </a>
        </v-card-title>
        <v-card-text class="py-2 white--text text-center">
          {{ new Date().getFullYear() }} — <strong>Mother Box Welcome</strong><br>
          Department of Computer Science, Faculty of Science, Prince of Songkla University 

        </v-card-text>
      </v-card>
    </v-footer>
  
  </v-app>
</template>

<script>
export default {
  name: 'AgeDp',
  data() {
    return {
      navbarColor: '#00bdd6',
      accessCode: '',
      adminEditDialog: false,
      showAlert: false,
      alertMessage: '',
      alertMessageLine2: '',
      alertColor: 'error',
      multiLine: false,
    };
  },
  methods: {
    goToHome() {
      if (this.$route.path !== '/') {
        this.$router.push({ path: '/' });
        this.navbarColor = '#00bdd6';
      }
    },
    goToAgeDp() {
      if (this.$route.path !== '/agedp') {
        this.$router.push({ path: '/agedp' });
        this.navbarColor = 'pink';
      }
    },
    goToMemory() {
      if (this.$route.path !== '/memory') {
        this.$router.push({ path: '/memory' });
        this.navbarColor = 'indigo';
      }
    },
    goToConduct() {
      if (this.$route.path !== '/conduct') {
        this.$router.push({ path: '/conduct' });
        this.navbarColor = 'teal';
      }
    },
    goToInfant() {
      if (this.$route.path !== '/infant') {
        this.$router.push({ path: '/infant' });
        this.navbarColor = 'green';
      }
    },
    goToHistory() {
      if (this.$route.path !== '/history') {
        this.$router.push({ path: '/history' });
        this.navbarColor = 'light brown';
      }
    },
    openAdminEdit() {
      this.adminEditDialog = true;
    },
    closeAdminEditDialog() {
      this.adminEditDialog = false;
      this.accessCode = '';
    },
    goToAdminEdit() {
      if (this.accessCode === '58645') {
        if (this.$route.path !== '/adminedit') {
          this.$router.push({ path: '/adminedit' });
          this.navbarColor = 'purple';
          this.closeAdminEditDialog();
        }
      } else {
       
        this.alertMessage = 'คุณกรอกรหัสเข้าระบบผิด';
        this.showAlert = true;
      }
    },
  },
};
</script>

<style lang="scss">
.admin-edit-button {
  background-color: purple;
  color: white;
  margin-left: 10px;
  padding: 5px 10px;
  border-radius: 5px;
}

.page-expandX-enter-active,
.page-expandX-leave-active {
  transition: transform 0.5s;
}

.page-expandX-enter,
page-expandX-leave-to {
  transform: scaleX(0);
}

.mothertext {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  margin-top: 50px;
  margin-bottom: 50px;
}

.image-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex;
}

.image-container2 {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex;
  margin-top: 60px;
}

.sd {
  background-image: url('~@/assets/99424962_128970812127339_4359640548470947840_n.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
  height: auto;
  width: auto;
}

.page-expandX-enter-active,
page-expandX-leave-active {
  transition: transform 0.7s;
}

page-expandX-enter,
page-expandX-leave-to {
  transform: scaleX(0);
}
</style>
