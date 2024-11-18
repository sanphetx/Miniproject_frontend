<template>
    <div>
      <v-row >
        
        <v-col>
          <div class="title-frame">
            <h1>พัฒนาการของทารก เดือนที่ 5 (สัปดาห์ที่ 18-21)</h1>
          </div >
        </v-col>

        
        <v-col >
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/19-20-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 19-20
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
                    ตอนนี้ทารกเริ่มดูดนิ้วตัวเองได้แล้ว ขนาดแขนและขาก็เริ่มสมส่วนกับร่างกาย สมองมีการขยายขนาดใหญ่ขึ้น สร้างเครือข่ายเส้นใยประสาทมากขึ้น และสมองกับกล้ามเนื้อต่างก็ช่วยกันทำหน้าที่ของตัวเองได้สัมพันธ์กันเป็นอย่างดี                               </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
  
       
        <v-col>
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/21-22-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 21-22
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
                    ทารกพัฒนาการดีขึ้น ภายนอกเหมือนทารกแรกคลอดแล้วแต่ภายในยังไม่สมบูรณ์เท่าไร  จึงยังไม่ใช่เวลาที่จะสามารถมีชีวิตอยู่ภายนอกโพรงมดลูกของคุณแม่ได้เพราะปอดและระบบการทำงานในอวัยวะบางอย่างยังไม่สมบูรณ์นั่นเอง                </v-card-text>
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