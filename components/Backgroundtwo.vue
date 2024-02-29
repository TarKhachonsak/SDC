<template>
  <div class="h-96 w-full relative bg-gradient-to-tr from-slate-800">
    <img src="public/backgroundimage2.jpg" alt="" class="w-full h-full object-cover">
    <div class="absolute top-1/2 left-1/3 transform -translate-x-1/3 -translate-y-1/2">
        <article class="text-wrap w-9/12 text-white drop-shadow-md">
            <p class="font-bold text-4xl pb-2">เมื่อครบกำหนดชำระค่าบริการที่ต้องจ่าย</p>
            <p>ท่านสามารถทำการโอนเงินผ่านธนาคารโดยใช้บัญชี หรือใช้บัตรเครดิตที่เชื่อมต่อกับบัญชีของท่าน กระบวนการนี้สามารถทำได้ผ่านช่องทางออนไลน์ซึ่งรวมถึงการใช้แอปพลิเคชันธนาคารหรือเว็บไซต์บริการการเงิน</p>
        </article>
        <div @click="submitForm" class="mt-5">
            <button class="bg-[#0075BE] hover:bg-[#005B94] text-white text-xl px-28 py-2 rounded-full">ชำระเงินที่นี่</button>
        </div>
    </div>
    
  </div>
</template>

<script>
export default {
  methods: {
  submitForm() {
    window.location.href = '/home/Billing';
  }
}
}
</script>
