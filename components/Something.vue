<template>
  <div class="my-20 mx-44">
    <div class="flex justify-center mx-44">
      <div class="h-[500px] relative pr-4">
          <img src="../public/pexels-life-of-pix-2459.jpg" class="w-full h-full object-cover mix-blend-overlay drop-shadow-xl">
      </div>
      <div class="grid grid-cols-3 gap-4">
          <div class="h-[230px] relative">
            <img src="../public/pexels-cottonbro-studio-5137980.jpg" class="w-full h-full object-cover drop-shadow-xl">
          </div>
          <div class="h-[230px] relative">
            <img src="../public/pexels-andrea-davis-12031595.jpg" class="w-full h-full object-cover drop-shadow-xl">
          </div>
          <div class="h-[230px] relative">
            <img src="../public/pexels-andrea-davis-12316662.jpg" class="w-full h-full object-cover drop-shadow-xl">
          </div>
          <div class="h-[250px] relative">
            <img src="../public/pexels-andrea-davis-12725828.jpg" class="w-full h-full object-cover drop-shadow-xl">
          </div>
          <div class="h-[250px] relative">
            <img src="../public/pexels-luis-quintero-2091634.jpg" class="w-full h-full object-cover drop-shadow-xl">
          </div>
          <div class="h-[250px] relative">
            <img src="../public/background1.jpg" class="w-full h-full object-cover drop-shadow-xl">
          </div>
      </div>
    </div>
    <div class="bg-[#304269] rounded-lg mx-44 my-10 flex items-center justify-between">
      <p class="text-white font-bold py-5 px-5">หอพักสุขใจ</p>
      <div @click="submitForm" class="mx-5">
          <button @click="submitForm" class="bg-[#D9E8F5] hover:bg-[#c9e6ff] px-5 py-2 rounded-xl">
            ดูห้องพักทั้งหมด
          </button>
      </div>
    </div>
    <div class="mx-44 bg-[#D9E8F5] rounded-md text-xl">
      <div class="px-5 py-5">
        <p>หอพักใกล้ มหาวิทยาลัยพะเยา หออยู่ซอย S2 ใกล้ประตู3 
          เดินทางง่าย ค่าไฟหน่วยละ 8 บาท ค่าน้ำเหมาจ่าย 100 บาท
          ห้องพักกว้างขวาง มีระเบียงทุกห้อง พัดลม 2,500-2800 บาท/เดือน
          แอร์ 3,200 บาท/เดือน มีที่จอดรถในร่ม เฟอร์นิเจอร์ในห้องมีเตียง 6 ฟุต ตู้เสื้อผ้า ทีวี พัดลม/แอร์
        </p>
        <div class="my-3">
          <p> เจ้าของหอพักใจดีสามารถติดต่อได้ตลอดเวลา 24 ชม.หากมีเหตุด่วน
              มีกล้องวงจรปิดทุกมุม ห้ามเลี้ยงสัตว์และห้ามส่งเสียงรบกวนยามวิกาล</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
  submitForm(){
    window.location.href = '/home/Slectroom';
  }
}
}
</script>

<style>

</style>