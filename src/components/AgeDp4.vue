<template>
    <div>
      <v-row >
        <v-col>
          <div class="title-frame">
            <h1>พัฒนาการของทารก เดือนที่ 4 (สัปดาห์ที่ 14-17)</h1>
          </div >
        </v-col>

       
        <v-col >
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/15-16-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 15-16
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
                    ช่วงหนึ่งสัปดาห์แรกของนั้น จะเรียกว่า “ตัวอ่อน” ตอนนี้หัวใจของทารกเต้นเร็วมาก หากคุณแม่อยากรู้ว่าเร็วขนาดไหนนั้น ลองนึกถึงอัตราการเต้นของหัวใจที่เร็วกว่าของแม่ประมาณเท่าตัวหรือประมาณ 140 – 150 ครั้งต่อนาที อวัยวะที่สำคัญก็เริ่มพัฒนาขึ้นอย่างรวดเร็ว 
                               </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
  
       
        <v-col>
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/17-18-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 17-18
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
                    “หนูเป็นทารกเต็มตัวแล้ว” ทารกเริ่มมีจมูกใหญ่ขึ้น มีกระดูก ซี่โครง เริ่มกลืนน้ำคร่ำและถ่ายปัสสาวะได้แล้วด้วยจ้ะ นอกจากนี้ทารกสามารถเริ่มเหยียดตัว งอหลังและยืนแขนขาได้ด้วย                </v-card-text>
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