<template>
 <Navbarown/>
    
    <!-- หัวข้อ -->
    <body>
        <div class="head items-center">
        <p id="head"></p>
        </div>
    </body>
    <div>
      <br>
        <p class="title"><b>การแจ้งเตือน</b></p>
    </div>
    <!-- --------- -->
    
    
    
  <div class="alerts">
    <alert-box v-for="(message, index) in messages" :key="index" :boxColor="index === 0 ? '#D9D9D9' : '#D9D9D9'">
      <span v-html="index === 0 ? coloredText(message) : message"></span>
    </alert-box>
  </div>

    <Footerown/> 
    
</template>

<script>
import AlertBox from './AlertBox.vue'; // เรียกใช้ AlertBox component

export default {
  components: {
    AlertBox
  },
  data() {
    return {
      messages: [
        "รายละเอียดการชำระค่าเช่าของห้องพัก A1 <span style='color: #3D9DD9;'>ชำระเสร็จสมบูรณ์</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องซักผ้าเครื่องที่ 1   <span style='color: #6E7346;'> ดำเนินการอยู่อีก 8 นาที</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องซักผ้าเครื่องที่ 2    <span style='color: #6E7346;'> งดใช้ชั่วคราว</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องซักผ้าเครื่องที่ 3 <span style='color: #3D9DD9;'>ว่าง</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องซักผ้าเครื่องที่ 4<span style='color: #6E7346;'>ดำเนินการอยู่อีก 58 นาที</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องกดน้ำเครื่องที่ 1 <span style='color: #6E7346;'>ดำเนินการอยู่อีก 5 นาที</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องกดน้ำเครื่องที่ 2  <span style='color: #3D9DD9;'>ว่าง</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องกดน้ำเครื่องที่ 3  <span style='color: #6E7346;'>งดใช้ชั่วคราว</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องกดน้ำเครื่องที่ 4<span style='color: #6E7346;'> ดำเนินการอยู่อีก 2 นาที</span> <span style='float: right;'>15/08/2590</span>",
        "แจ้งให้ทราบในวันที่ 16/08/2590 การไฟฟาแจ้งว่าจะมีการตัดไฟเพื่อซ่อมบำรุงบริเวณหอพักของเรา ในเวลา 08:00 - 16:00 น. <br>จึงขอแจ้งให้ทราบและขออภัยในความไม่สะดวก<span style='float: right;'>15/08/2590</span>",
        "แจ้งให้ทราบในวันที่ 16/08/2590 การประปาแจ้งว่าจะมีการตัดไฟเพื่อซ่อมบำรุงบริเวณหอพักของเรา ในเวลา 08:00 - 09:00 น. <br>จึงขอแจ้งให้ทราบและขออภัยในความไม่สะดวก<span style='float: right;'>15/08/2590</span>",
        
      ]
    };
  },
  methods: {
    coloredText(message) {
      return message.replace(/<span style='color: #3D9DD9;'>/g, "<span style='color: #3D9DD9;'>");
      return message.replace(/<span style='color: #6E7346;'>/g, "<span style='color: #6E7346;'>");
    }
  }
  
};
</script>
<style scoped>


.title {
  margin-left: 100px;
  font-size: larger;
}

</style>