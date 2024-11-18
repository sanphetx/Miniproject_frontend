<template>
    
      <v-row class="sd" clos="12">
          <v-col clos="12">
          <Infant/>
      </v-col>
      </v-row>
   
  </template>
  
  <script>
  export default {
      components:{
        Infant: () => import('../components/Infant.vue')
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