<template>
    <v-container>
      <v-row>
          <v-col clos="12">
          <Memory/>
      </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
      components:{
        Memory: () => import('../components/Memory.vue')
      }
  }   
  </script>
  
  <style>
  
  </style>