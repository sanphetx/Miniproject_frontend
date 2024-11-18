<template>
    <div>
      <v-row >
        
        <v-col>
          <div class="title-frame">
            <h1>พัฒนาการของทารก เดือนที่ 9 (สัปดาห์ที่ 36-40)</h1>
          </div >
        </v-col>

       
        <v-col >
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/37-38-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 37-38
            </v-card-title>
            <v-card-subtitle>
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
                <v-card-text>
                  ตอนนี้ทารกแข็งแรง ฉลาด มีเซลล์ประสาทมากด้วยนะ หากทารกเป็นผู้หญิงมดลูกและท่อรังไข่จะสร้างเสร็จสมบูรณ์และอยู่ในตำแหน่งที่ถูกต้อง แต่ถ้าหากทารกเป็นผู้ชายก็จะสามารถมองเห็นอวัยวะเพศได้ชัดเจน ขนาดตัวตอนนี้อยู่ที่ประมาณ  45 – 49  เซนติเมตร น้ำหนัก 2,100 – 2,700 กรัม</v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
  
       
        <v-col>
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/39-40-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 39-40
            </v-card-title>
            <v-card-subtitle>
              ดูรายละเอียด
            </v-card-subtitle>
            <v-card-actions>
              <v-btn icon @click="show2 = !show2">
                <v-icon>{{ show2 ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
              </v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show2">
                <v-divider></v-divider>
                <v-card-text>
                  ทารกพร้อมออกมาดูโลกแล้ว ปอดของลูกน้อยพัฒนาเต็มที่ พร้อมที่จะหายใจหลังคลอดแล้ว อวัยวะทุกส่วนเจริญเติบโตเต็มที่ฮอร์โมนจากรกจะช่วยเตรียมเต้านมคุณแม่ให้ผลิตน้ำนม และอาจทำให้หนูมีเต้านมและหัวนมที่เต่งตึงได้ด้วย แต่ไม่ต้องห่วง เพราะอาการจะหายไปเองใน 2- 3 วัน ตอนนี้ทารกตัวอ้วนกลมอยู่เต็มโพรงมดลูกของแม่แล้วละ ลำตัวตัวยาวประมาณ 49-51 เซนติเมตร น้ำหนัก 2,800-3,000 กรัม                 </v-card-text>
              </div>
            </v-expand-transition>
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
    
      
    }),
  };
  </script>
  <style>
.title-frame {
  border: 2px solid #007BFF; 
  box-shadow: 0px 0px 10px #007BFF; 
  text-align: center;
  padding: 10px;
  border-radius: 10px; 
}

.title-frame h1 {
  font-size: 24px; 
  margin: 0;
}
.v-card {
  margin-top: 100px; 
}
</style>