<template>
  <Navbarown class="mb-4"/>

  <div class="rounded-box ">
    <img src="/nadeach.jpg" class="image rounded-full w-[150px] h-[150px]" />
    <div class="infomation1">
      <ul>
        <li class="p-4"><b> ชื่อ</b> : ผู้ใช้ และ นามสกุล</li>
        <li class="p-4"><b> เบอร์โทรศัพท์</b> : 099-9999999</li>
        <li class="p-4"><b>เริ่มทำสัญญาเมื่อ</b> วัน กรกฎาคม 2465</li>
      </ul>
    </div>

    <div class="infomation1">
      <ul>
        <li class="p-4"><b> ชื่อเล่น</b>: ผู้เช่า</li>
        <li class="p-4"><b>อีเมล</b>: aaaaaa@gimi.com</li>
        <li class="p-4"><b>เพศ</b>: หญิง</li>
      </ul>
    </div>
  </div>

  <div class="box">
    <div class="ct bg-white w-[700px] h-[590px]">
      <div class="mt-2" id="font">4 nov 2547</div>
      <br />
      <div class="went">
        <div class="bc">ขออณุญาตเปิดห้องนะคะ มีช่างมาซ่อมแอร์ค่ะ</div>
      </div>
      <br />
      <div class="went1">
        <div class="bc1">ครับ วันนี้ผมไปเรียนครับ</div>
      </div>
      <br />
      <br />
      <br />
      <br />
      <br />
      <br />
      <br />
      <br />
      <br />
      <br />
      <br />
      <br />
      <br />

      <div class="chat">
        <div v-for="message in messages" :key="message.id">
          <p>{{ message.text }}</p>
        </div>
        <input
          v-model="newMessage"
          @keyup.enter="sendMessage"
          placeholder="Type your message here"
        />
        <i class="fa fa-camera" aria-hidden="true"></i>
        <i class="fa fa-microphone" aria-hidden="true"></i>
      </div>
    </div>
  </div>

  <Footerown  class="mt-4"/>
</template>

<script>
export default {
  name: "RoundedBox",
};
</script>

<style>
.rounded-box {
  width: 700px; /* กำหนดความกว้าง */
  height: 20%; /* กำหนดความสูง */
  background-color: #d9e8f5; /* กำหนดสีพื้นหลัง */
  border-radius: 10px 10px 0% 0%; /* กำหนดให้มุมโค้งทั้งหมดเป็น 50% */
  border: 10px solid;
  border-color: #33a9f7;
  display: flex;
  margin: auto;
  padding-left: 1%;
  padding: 1%;
}
.image {
  border: solid rgb(255, 255, 255);
  border-radius: 100px;
  border-width: 0.1cm;
}
.infomation1 {
  font-size: 16px;
}
.box {
  width: 700px; /* กำหนดความกว้าง */
  height: 600px; /* กำหนดความสูง */
  background-color: #ffffff; /* กำหนดสีพื้นหลัง */
  border-radius: 0% 0% 5% 5%; /* กำหนดให้มุมโค้งทั้งหมดเป็น 50% */
  border: 10px solid;
  border-color: #33a9f7;
  display: flex;
  margin: auto;
  border-top: 2px;
}
.chat {
  padding: 10px;
  border-radius: 5px;
}

input {
  width: 86%;
  padding: 8px;
  margin-top: 5px;
  border-radius: 5px;
  border: 1px solid #646464;
  background: gainsboro;
}
.ct {
  border-radius: 0% 0% 3% 3%;
}
.bc {
  background-color: #d9e8f5;
  width: 340px;
  height: 60px;
  text-align: center;
  display: flex;
  padding: 3%;
  border-radius: 20px;
  border: 5px solid;
  border-color: #3d9dd9;
}
.went {
  padding-left: 47%;
}
.went1 {
  padding-left: 3%;
}
#font {
  color: gray;
  margin: center;
  text-align: center;
}
.bc1 {
  background-color: #ffffff;
  width: 200px;
  height: 60px;
  text-align: center;
  display: flex;
  border-radius: 20px;
  border: 5px solid;
  border-color: #3d9dd9;
  padding: 2%;
}
.fa {
  padding: 2%;
}
</style>