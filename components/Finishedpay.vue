<template>
  <div class="flex justify-center items-center bg-[#D9E8F5]">
    <div class="my-36 w-3/12 bg-[#FAFAFA] flex flex-col justify-center items-center rounded-sm drop-shadow-[2px_2px_rgba(0,0,0,0.25)]">
        <div>
            <p class="font-bold text-3xl mt-3">ชำระเงินสำเร็จ</p>
        </div>
        <div class="py-12 size-4/5">
            <img src="../public/correct.png" alt="">
        </div>
        <div @click="submitForm" class="mb-3 bg-[#0075BE]">
            <button class="hover:bg-[#005B94] text-xl text-white p-2 rounded-sm">
                กลับไปที่หน้าหลัก
            </button>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
  submitForm() {
    window.location.href = '/home';
  }
}
}
</script>

<style>

</style>
