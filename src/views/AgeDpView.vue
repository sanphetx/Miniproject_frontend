<template>
    
      <v-row>
          <v-col class="sd" clos="12">
          <AgeDp/>
      </v-col>
      </v-row>
   
  </template>
  
  <script>
  export default {
      components:{
          AgeDp: () => import('../components/AgeDp.vue')
      }
  }   
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