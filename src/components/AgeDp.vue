<template >

    <v-container>
     <div class="title-frame">
        <h1 class="mothertext">พัฒนาการ <span class="heart-box">ของทารกในครรภ์</span></h1> 
      </div>
      <div class="image-container">
        <v-card
            class="mx-auto card-with-animation"
            max-width="400"
            @mouseenter="startCardAnimation"
            @mouseleave="stopCardAnimation"
          >
  <v-img
    src="../assets/1-1.png"
    height="65%"
   
  ></v-img>
  <v-card-title>
      อายุครรภ์ 1-4 สัปดาห์    </v-card-title>
  <v-card-actions>
    <v-btn color="orange lighten-2" @click="goToAgeDp(0)">ดูรายละเอียด</v-btn> 
  </v-card-actions>
</v-card>
<v-card
            class="mx-auto card-with-animation"
            max-width="400"
            @mouseenter="startCardAnimation"
            @mouseleave="stopCardAnimation"
          >
  <v-img
    src="../assets/2-2.png"
    height="65%"
  ></v-img>
  <v-card-title>
     อายุครรภ์ 5-8 สัปดาห์   </v-card-title>
  <v-card-actions>
    <v-btn color="orange lighten-2" @click="goToAgeDp(1)">ดูรายละเอียด</v-btn> 
  </v-card-actions>
</v-card>
<v-card
            class="mx-auto card-with-animation"
            max-width="400"
            @mouseenter="startCardAnimation"
            @mouseleave="stopCardAnimation"
          >
  <v-img
    src="../assets/3-3.png"
    height="65%"
  ></v-img>
  <v-card-title>
    อายุครรภ์ 9-13 สัปดาห์   </v-card-title>
  <v-card-actions>
    <v-btn color="orange lighten-2" @click="goToAgeDp(2)">ดูรายละเอียด</v-btn> 
  </v-card-actions>
</v-card>
<v-card
            class="mx-auto card-with-animation"
            max-width="400"
            @mouseenter="startCardAnimation"
            @mouseleave="stopCardAnimation"
          >
  <v-img
    src="../assets/4-4.png"
    height="65%"
  ></v-img>
  <v-card-title>
    อายุครรภ์ 14-17 สัปดาห์   </v-card-title>
  <v-card-actions>
    <v-btn color="orange lighten-2" @click="goToAgeDp(3)">ดูรายละเอียด</v-btn> 
  </v-card-actions>
</v-card>
<v-card
            class="mx-auto card-with-animation"
            max-width="400"
            @mouseenter="startCardAnimation"
            @mouseleave="stopCardAnimation"
          >
  <v-img
    src="../assets/5-5.png"
    height="65%"
  ></v-img>
  <v-card-title>
    อายุครรภ์ 18-21 สัปดาห์   </v-card-title>
  <v-card-actions>
    <v-btn color="orange lighten-2" @click="goToAgeDp(4)">ดูรายละเอียด</v-btn> 
  </v-card-actions>
</v-card>
<v-card
            class="mx-auto card-with-animation"
            max-width="400"
            @mouseenter="startCardAnimation"
            @mouseleave="stopCardAnimation"
          >
</v-card>
      </div>
      <div class="image-container2">
        <v-card
            class="mx-auto card-with-animation"
            max-width="400"
            @mouseenter="startCardAnimation"
            @mouseleave="stopCardAnimation"
          >
  <v-img
    src="../assets/6-6.png"
    height="65%"
  ></v-img>
  <v-card-title>
    อายุครรภ์ 22-26 สัปดาห์ </v-card-title>
  <v-card-actions>
    <v-btn color="orange lighten-2" @click="goToAgeDp(5)">ดูรายละเอียด</v-btn> 
  </v-card-actions>
</v-card>
<v-card
            class="mx-auto card-with-animation"
            max-width="400"
            @mouseenter="startCardAnimation"
            @mouseleave="stopCardAnimation"
          >
  <v-img
    src="../assets/7-7.png"
    height="65%"
  ></v-img>
  <v-card-title>
    อายุครรภ์ 27-30 สัปดาห์    </v-card-title>
  <v-card-actions>
    <v-btn color="orange lighten-2" @click="goToAgeDp(6)">ดูรายละเอียด</v-btn> 
  </v-card-actions>
</v-card>
<v-card
            class="mx-auto card-with-animation"
            max-width="400"
            @mouseenter="startCardAnimation"
            @mouseleave="stopCardAnimation"
          >
  <v-img
    src="../assets/8-8.png"
    height="65%"
  ></v-img>
  <v-card-title>
    อายุครรภ์ 31-35 สัปดาห์   </v-card-title>
  <v-card-actions>
    <v-btn color="orange lighten-2" @click="goToAgeDp(7)">ดูรายละเอียด</v-btn> 
  </v-card-actions>
</v-card>
<v-card
            class="mx-auto card-with-animation"
            max-width="400"
            @mouseenter="startCardAnimation"
            @mouseleave="stopCardAnimation"
          >
  <v-img
    src="../assets/9-9.png"
    height="65%"
  ></v-img>
  <v-card-title>
    อายุครรภ์ 36-40 สัปดาห์    </v-card-title>
  <v-card-actions>
    <v-btn color="orange lighten-2" @click="goToAgeDp(8)">ดูรายละเอียด</v-btn> 
  </v-card-actions>
</v-card>
      </div>
    </v-container>
  
</template>

<script>
export default {
  name: 'AgeDp',
  methods: {
    goToAgeDp(index) {
      const paths = [
        '/agedp1',
        '/agedp2',
        '/agedp3',
        '/agedp4',
        '/agedp5',
        '/agedp6',
        '/agedp7',
        '/agedp8',
        '/agedp9',
      ];

      this.$router.push({ path: paths[index] }).catch(() => {});
    },

    startCardAnimation(event) {
      const card = event.target;
      card.classList.add('animated');
    },

    stopCardAnimation(event) {
      const card = event.target;
      card.classList.remove('animated');
    },
  },
};
</script>


<style lang="scss">
.mothertext {
  display: flex;
  flex-wrap: wrap;
  justify-content: center; 
  align-items: center; 
  margin-top: 50px;
  margin-bottom: 50px;
}

.card-with-animation {
  transition: transform 0.3s ease;
}

.card-with-animation.animated {
  transform: scale(1.1);
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
.mothertext {
  text-align: center;
  margin-top: 50px;
  margin-bottom: 50px;
  font-size: 28px;
}

/* สร้าง animation ดุ๊กดิ๊ก */
@keyframes textAnimation {
  0% {
    transform: scale(1);
  }
  25% {
    transform: scale(1.1);
  }
  50% {
    transform: scale(0.9);
  }
  75% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}

.title-frame h1 {
  font-size: px; 
  margin: 0;
}

.top-left-image {
    position: absolute;
    top: 0;
    left: 0;
    width: 20%; 
  }

  .top-right-image {
    position: absolute;
    top: 0;
    right: 0;
    width: 20%; 
  }

  .title-frame {
    border: 2px solid #ddd;
    padding: 20px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    text-align: center;
    margin-top: 50px;
    margin-bottom: 50px;
    transition: transform 0.5s ease-in-out;
  }

  .title-frame:hover {
    transform: scale(1.05);
  }

  .mothertext {
    font-size: 28px;
    color: #333;
    font-family: 'Fredoka One', cursive;
    animation: textAnimation 1s ease-in-out;
  }

  .heart-box {
    color: #ff69b4;
    font-weight: bold;
    animation: heartbeat 2s infinite;
  }
</style>