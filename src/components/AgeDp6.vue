<template>
    <div>
      <v-row >
        <v-col>
          <div class="title-frame">
            <h1>พัฒนาการของทารก เดือนที่ 6 (สัปดาห์ที่ 22-26)</h1>
          </div >
        </v-col>

        <v-col >
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/23-24-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 23-24
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
                  ตอนนี้ทารกรู้สึกสนุกกับการเรียนรู้และตอบโต้แม่มาก ๆ เลยละ ไม่ว่าแม่จะพูดหรือคุยกับใครทารกได้ยินชัดแจ๋วเลย ที่สำคัญเสียงสุนัขที่บ้านเห่า เสียงแตรรถยนต์หรือเสียงเพลงที่ดังมาก ๆ ยิ่งได้ยินหมดเลย และตอนนี้ทารกของแม่มีขนาด 22 – 28 เซนติเมตร และน้ำหนักประมาณ 400-600 กรัมแล้วนะ                   </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
  
        <v-col>
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/25-26-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 25-26
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
                  ครึ่งทางแล้ว ตอนนี้ทารกสามารถเคลื่อนไหวได้ตามเสียงหรือจังหวะการเคลื่อนไหวของแม่แล้ว อวัยวะหูภายนอกของทารกก็พัฒนาสมบูรณ์ ช่วงนี้แม่ต้องพูดกับทารกบ่อย ๆ นะ ทารกจะได้จำเสียงของคุณแม่ได้                    </v-card-text>
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