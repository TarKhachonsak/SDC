<template>
    <Navbarown />
    <Background />
    <Menuown />

  <div class="h-96 w-full relative bg-gradient-to-tr from-slate-800">
    <img src="public/backgroundimage2.jpg" alt="" class="w-full h-full object-cover">
    <div class="absolute top-1/2 left-1/3 transform -translate-x-1/3 -translate-y-1/2">
        <article class="text-wrap w-9/12 text-white drop-shadow-md">
            <p class="font-bold text-4xl pb-2">เมื่อครบกำหนดชำระค่าบริการที่ต้องจ่าย</p>
            <p>ท่านสามารถทำการโอนเงินผ่านธนาคารโดยใช้บัญชี หรือใช้บัตรเครดิตที่เชื่อมต่อกับบัญชีของท่าน กระบวนการนี้สามารถทำได้ผ่านช่องทางออนไลน์ซึ่งรวมถึงการใช้แอปพลิเคชันธนาคารหรือเว็บไซต์บริการการเงิน</p>
        </article>
    </div>
  </div>
    <Howtopay />
    <Footerown />

</template>

<script>
export default {
  name: 'Home'
}
</script>