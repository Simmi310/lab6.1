<script setup>
import { ref } from "vue";
var person = ref({
  day: "",
  name: "",
  id: "",
  engname: "",
  idper: "",
  major: "",
  group: "",
  tel: "",
  noatm: "",
  atm: "",
  lost: "",
  cant: "",
  newst: "",
  error: "",
  rename: "",
  exx: "",
  move: "",
  out: "",
  lastday: "",
});
var show = ref(false);
</script>
<template>
  <div class="d-flex justify-content-center align-items-center mt-5">
    <div>
      <div>
        <div>
          <h1>แบบฟอร์มขอทำบัตรประจำตัวนักศึกษา</h1>
          <br />
        </div>
        <div>
          <input type="date" v-model="person.day" /><br />
           ข้าพเจ้า(ชื่อ-นามสกุล)
          <input type="text" v-model="person.name" />
           รหัสนักศึกษา
          <input type="text" v-model="person.id" /><br />
          ชื่อภาษาอังกฤษ
          <input type="text" v-model="person.engname" />
          เลขประจำตัวประชาชน
          <input type="text" v-model="person.idper" /><br />
          สาขาวิชา
          <select name="selectgrop" v-model="person.major">
            <option value="คณะผลิตกรรมการเกษตร">คณะผลิตกรรมการเกษตร</option>
            <option value="คณะบริหารธุรกิจ">คณะบริหารธุรกิจ</option>
            <option value="คณะวิทยาศาสตร์">คณะวิทยาศาสตร์</option>
            <option value="คณะศิลปศาสตร์">คณะศิลปศาสตร์</option>
            <option value="คณะสถาปัตยกรรมศาสตร์ และการออกแบบสิ่งแวดล้อม ">
              คณะสถาปัตยกรรมศาสตร์ และการออกแบบสิ่งแวดล้อม
            </option>
            <option value="คณะเทคโนโลยีการประมง และทรัพยากรทางน้ำ">
              คณะเทคโนโลยีการประมง และทรัพยากรทางน้ำ
            </option>
            <option value="คณะวิศวกรรมและอุตสาหกรรมเกษตร ">
              คณะวิศวกรรมและอุตสาหกรรมเกษตร
            </option>
            <option value="คณะพัฒนาการท่องเที่ยว ">คณะพัฒนาการท่องเที่ยว</option>
            <option value="คณะเศรษฐศาสตร์ ">คณะเศรษฐศาสตร์</option>
            <option value="วิทยาลัยบริหารศาสตร์ ">วิทยาลัยบริหารศาสตร์</option>
            <option value="วิทยาลัยพลังงานทดแทน ">วิทยาลัยพลังงานทดแทน</option>
            <option value="วิทยาลัยนานาชาติ ">วิทยาลัยนานาชาติ</option>
            <option value="มหาวิทยาลัยแม่โจ้-แพร่ เฉลิมพระเกียรติ ">
              มหาวิทยาลัยแม่โจ้-แพร่ เฉลิมพระเกียรติ
            </option>
            <option value="มหาวิทยาลัยแม่โจ้-ชุมพร ">มหาวิทยาลัยแม่โจ้-ชุมพร</option>
            <option value="คณะพยาบาลศาสตร์">คณะพยาบาลศาสตร์</option>
            <option value="คณะสัตวแพทย์ศาสตร์">คณะสัตวแพทย์ศาสตร์</option></select
          ><br />
          คณะ
          <select name="" v-model="person.group">
            <option value="คณะผลิตกรรมการเกษตร">คณะผลิตกรรมการเกษตร</option>
            <option value="คณะวิศวกรรมเเละอุตสาหกรรม">คณะวิศวกรรมเเละอุตสาหกรรม</option>
            <option value="คณะวิทยาศาสตร์">คณะวิทยาศาสตร์</option>
            <option value="คณะวิทยาลัยบริหารศาสตร์">คณะวิทยาลัยบริหารศาสตร์</option>
            <option value="คณะบริหารธุรกิจ">คณะบริหารธุรกิจ</option>
            <option value="คณะพัฒนาการท่องเที่ยว">คณะพัฒนาการท่องเที่ยว</option>
            <option value="คณะเทคโนโลยีการประมงเเละทรัพยากรทางน้ำ">
              คณะเทคโนโลยีการประมงเเละทรัพยากรทางน้ำ
            </option>
            <option value="คณะเศรษฐศาสตร์">คณะเศรษฐศาสตร์</option>
            <option value="คณะศิลปศาสตร์">คณะศิลปศาสตร์</option>
            <option value="คณะวิทยาลัยพลังงานทดเเทน">คณะวิทยาลัยพลังงานทดเเทน</option>
            <option value="คณะสารสนเทศเเละการสื่อสาร">คณะสารสนเทศเเละการสื่อสาร</option>
            <option value="คณะสถาปัตยกรรมศาสตร์เเละการออกเเบบสิ่งเเวดล้อม">
              คณะสถาปัตยกรรมศาสตร์เเละการออกเเบบสิ่งเเวดล้อม
            </option>
            <option value="คณะสัตวศาสตร์เเละเทคโนโลยี">คณะสัตวศาสตร์เเละเทคโนโลยี</option>
            <option value="มหาวิทยาลัยเเม่โจ้-เเพร่ เฉลิมพระเกีตรติ">
              มหาวิทยาลัยเเม่โจ้-เเพร่ เฉลิมพระเกีตรติ
            </option>
            <option value="มหาวิทยาลัยเเม่โจ้-ชุมพร">
              มหาวิทยาลัยเเม่โจ้-ชุมพร
            </option></select
          ><br />
          เบอร์โทรศัพท์
          <input type="text" v-model="person.tel" />มีความประสงค์ขอทำบัตรประจำตัวนักศึกษา
          <br />
          <input type="checkbox" v-model="person.noatm" />
          บัตรรูปแบบของมหาวิทยาลัย(ไม่ใช้ATM) ระยะการดำเนินการไม่ถึง 1 สัปดาห์ <br />
          <input type="checkbox" v-model="person.atm" /> บัตรรูปแบบของธนาคาร(ATM)
          ระยะการดำเนินการไม่ถึง 1 เดือน
          <br />
          โดยมีเหตุผลดังนี้ <br />
          <input type="checkbox" v-model="person.lost" /> บัตรเดิมสูญหาย <br />
          <input type="checkbox" v-model="person.cant" /> บัตรถูกอายัติ <br />
          <input type="checkbox" v-model="person.newst" />
          กรณีที่นักศึกษามารายงานตัวเข้าเป็นนักศึกษาใหม่หลังกำหนด
          <br />
          ในกรณีต่อไปนี้ นักศึกษาต้องเเนบบัตรประจำตัวนักศึกษาเดิม <br />
          <input type="checkbox" v-model="person.error" /> บัตรชำรุด <br />
          <input type="checkbox" v-model="person.rename" /> เปลี่ยนชื่อ-นามสกุล <br />
          <input type="checkbox" v-model="person.exx" /> บัตรหมดอายุ <br />
          <input type="checkbox" v-model="person.move" /> โอนย้ายสาขาวิชา <br />
          วันออกบัตร
          <input type="date" v-model="person.out" />
          วันหมดอายุ
          <input type="date" v-model="person.lastday" />
        </div>
      </div>
      <div>
        <button @click=" show = !show">ส่ง</button>
        <div v-if="show ">
          {{ person }}
        </div>
      </div>
    </div>
  </div>
</template>
