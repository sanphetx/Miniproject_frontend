<template>
    
      
      <v-row>
        <v-col class="sd" clos="12">
          <AgeDp4 />
          <v-btn @click="goToAgeDp">กลับไปยังหน้า AgeDp</v-btn>
        </v-col>
      </v-row>
      
    
  </template>
  
  <script>
  export default {
    components: {
      AgeDp4: () => import('../components/AgeDp4.vue')
    },
    methods: {
      goToAgeDp() {
        this.$router.push({ path: '/agedp' }).catch(() => {});
      },
    },
  };
  </script>
  
  <style>
  .sd {
    background-image: url('~@/assets/99424962_128970812127339_4359640548470947840_n.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-attachment: fixed;
    height: auto;
    width: auto;
  }
  </style>
    