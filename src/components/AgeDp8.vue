<template>
    <div>
      <v-row >
        
        <v-col>
          <div class="title-frame">
            <h1>พัฒนาการของทารก เดือนที่ 8 (สัปดาห์ที่ 31-35)</h1>
          </div >
        </v-col>

        
        <v-col >
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/31-34-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 27-28
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
                  ตอนนี้ทารกกะพริบตาได้ ประสาทสัมผัสทั้ง 5 เริ่มทำงานได้ดีและสมบูรณ์ สมองก็พัฒนาเต็มที่ต่อเนื่อง ช่วยให้ตา กล้ามเนื้อ และปอดทำงานได้ดีขึ้น นอกจากนี้ ไม่ว่าแม่จะทานอะไร ทารกก็รับรส รับกลิ่น ได้ยิน และสัมผัสได้ดีขึ้นแล้ว</v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
  
       
        <v-col>
            <v-card class="mx-auto" max-width="344" style="box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.8);">            <v-img
              src="../assets/apd/29-30-Week-794x1024.webp"
              height="400px"
            ></v-img>
            <v-card-title>
              สัปดาห์ ที่ 35-36
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
                  ท้องแม่เริ่มเล็กเกินไปสำหรับทารกแล้ว ผิวหนังของทารกก็ยังคงสร้างชั้นไขมันอยู่เรื่อย ๆ เพื่อรักษาอุณหภูมิร่างกายให้อบอุ่น จึงยังคงมีไขสีขาวอยู่บ้างบริเวณลำตัวและหลัง เพื่อช่วยหล่อลื่นให้คลอดได้ง่ายขึ้น ตอนนี้ยาว 42-45 เซนติเมตร น้ำหนัก 1,700-2,000 กรัมแล้วนะ
                </v-card-text>
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