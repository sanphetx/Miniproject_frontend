<template>
    <div>
      <v-row >
        <v-col>
          <div class="title-frame">
            <h1>พัฒนาการของทารก เดือนที่ 1 (สัปดาห์ที่ 1-4)</h1>
          </div >
          <h1>พัฒนาการของทารก เดือนที่ 1 (สัปดาห์ที่ 1-4)</h1>
        </v-col>

        <v-col >
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/1-Week-794x1024.jpg"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 1
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
                    ช่วงหนึ่งสัปดาห์แรกของนั้น จะเรียกว่า “ตัวอ่อน” ช่วงนี้เป็นช่วงที่ทารกได้รับทั้งสารอาหารพร้อมกับขับถ่ายของเสียผ่านเยื่อหุ้มรกที่กำลังจะพัฒนาเป็นรกกับเส้นเลือดในผนังมดลูกของแม่                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
  
        
        <v-col>
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/2-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 2
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
                    เมื่อเข้าสัปดาห์ที่สอง ร่างกายของทารกเริ่มมีการสร้างไขสันหลังและส่วนหลัง โดยจะพัฒนาไปเป็นโครงสร้างกระดูกสันหลังและสมอง และทารกเริ่มมี “หัวใจ” ดวงน้อย ๆ แล้ว                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
  
        
        <v-col>
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/3-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 3
            </v-card-title>
            <v-card-subtitle>
              ดูรายละเอียด
            </v-card-subtitle>
            <v-card-actions>
              <v-btn icon @click="show3 = !show3">
                <v-icon>{{ show3 ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
              </v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show3">
                <v-divider></v-divider>
                <v-card-text>
                    ทารกฝังตัวอยู่ในผนังมดลูกของแม่และเริ่มแบ่งกลุ่มเซลล์ออกเป็น 3 กลุ่ม ได้แก่ “กลุ่มชั้นนอก” ที่จะมาช่วยพัฒนาเป็นระบบประสาท ผิวหนัง ฟัน ผม เลนส์ตา และต่อมต่าง ๆ ต่อไปเป็น “กลุ่มชั้นกลาง” ที่จะมาพัฒนาเป็นระบบกล้ามเนื้อ อวัยวะสืบพันธุ์ ระบบขับถ่าย เส้นเลือดหัวใจ และกระดูก และกลุ่มสุดท้ายก็คือ “กลุ่มชั้นใน” จะพัฒนาเป็นระบบย่อย อวัยวะหายใจ ตับ และตับอ่อน นั่นเอง                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
  
        
        <v-col>
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">
            <v-img
              src="../assets/apd/4-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 4
            </v-card-title>
            <v-card-subtitle>
              ดูรายละเอียด
            </v-card-subtitle>
            <v-card-actions>
              <v-btn icon @click="show4 = !show4">
                <v-icon>{{ show4 ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
              </v-btn>
            </v-card-actions>
            <v-expand-transition>
              <div v-show="show4">
                <v-divider></v-divider>
                <v-card-text>
                    ตอนนี้ขนาดของทารกเล็กเท่าปลายเข็ม ร่างกายของทารกกำลังสร้างเลือดและเส้นเลือดอย่างรวดเร็ว เพราะทารกต้องใช้ออกซิเจนและสารอาหารจากแม่เพื่อช่วยในการเจริญเติบโต โดยทั้งสองอย่างนั้นจะถูกถ่ายทอดลำเลียงผ่านท่อเล็กจิ๋วที่เชื่อมระหว่างตัวอ่อนและหลอดเลือดในผนังมดลูกของแม่                </v-card-text>
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
      show3: false,
      show4: false,
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