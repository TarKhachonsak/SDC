<template>
  <div class="relative bg-[#D9E8F5]">
    <div class="p-24 flex justify-center">
        <img src="../public/Slice 3.png" alt="">
        <button @click="submitForm" class="absolute bottom-1/4 right-1/3  bg-[#0075BE] hover:bg-[#005B94]">
            <p class="px-20 py-2 text-white text-xl font-bold rounded-sm">ไปที่หน้าชำระเงิน</p>
        </button>
    </div>
</div>

</template>

<script>
export default {
  methods: {
  submitForm() {
    window.location.href = '/home/Pay';
  }
}
}
</script>

<style>

</style>