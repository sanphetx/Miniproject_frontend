<template>
 
    <v-row >
        <v-col class="x" clos="12">
          <HelloWorld />
    </v-col>
    </v-row>
    

  
</template>

<script>
import HelloWorld from '../components/HelloWorld'

export default {
  name: 'Home',

  components: {
    HelloWorld
  }
}
</script>
<style>
.x {
  background-image: url('~@/assets/117542534_xl-scaled.webp');
  background-size: cover;
  height: 100vh; 
  width: 100%;
 
}
</style>