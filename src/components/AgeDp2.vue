<template>
  <div>
    <v-row>
      <v-col>
        <div class="title-frame">
          <h1>พัฒนาการของทารก เดือนที่ 2 (สัปดาห์ที่ 5-8)</h1>
        </div>
        
        <div>
          <v-card-title class="subtitle-text">
            
  สัปดาห์ ที่ 5-8
</v-card-title>
<v-card-subtitle class="subtitle-text">
  ดูรายละเอียด
</v-card-subtitle>
          <v-card-actions>
            <v-btn icon @click="show1 = !show1">
              <v-icon>{{ show1 ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
            </v-btn>
          </v-card-actions>
          <v-expand-transition>
            <div v-show="show1">
              <v-divider></v-divider>
              <v-card-text class="card-text">
                ตอนนี้รูปร่างของทารกเหมือนกุ้งที่กำลังงอตัว ที่พิเศษไปกว่านั้นก็คือ ร่างกายสามารถเริ่มแยกได้แล้วว่าส่วนไหนเป็นส่วนของศีรษะ ลำตัว แขนละขา ลำตัวของทารกเริ่มจะค่อย ๆ ยืดยาวออกทีละนิด พร้อมกับเค้าโครงหน้าก็เริ่มปรากฎเป็น จมูก ปาก โพรงจมูก และก็ช่องปากแล้วนะ
              </v-card-text>
              
            </div>
            
          </v-expand-transition>
          
        </div>
        
      </v-col>

      
      <v-col>
        <v-card class="mx-auto" max-width="500" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">
          <v-img
              src="../assets/apd/5-8-Week-794x1024.webp"
              height="600px"
              style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);"
          ></v-img>
          
        </v-card>
      </v-col>
    </v-row>
    
  </div>
  
</template>

<script>
export default {
data: () => ({
  show1: false,
  show2: false,
  show3: false,
  show4: false,
}),
};
</script>

<style>
.title-frame {
border: 2px solid #007BFF; 
box-shadow: 0px 0px 10px #007BFF;
padding: 10px;
border-radius: 10px; 
margin-top: 30px;
}

.title-frame h1 {
font-size: 28px; 
margin: 0;
}

.card-text {
font-size: 20px; 
}

.v-card {
margin-top: 100px; 
}
.subtitle-text {
  font-size: 20px;
}
</style>
