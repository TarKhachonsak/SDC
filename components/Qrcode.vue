<template>
  <div class="flex justify-center items-center bg-[#D9E8F5]">
    <div class="my-36 w-3/12 bg-[#FAFAFA] flex flex-col justify-center items-center rounded-sm drop-shadow-[2px_2px_rgba(0,0,0,0.25)]">
        <div>
            <p class="font-bold text-3xl mt-3">ชำระเงิน</p>
        </div>
        <div class=" py-12 size-4/5">
            <img src="public/qrcode.png">
        </div>
        <div class="mb-3 bg-[#0075BE]">
            <button @click="submitForm" class="hover:bg-[#005B94] text-xl text-white p-2 rounded-sm">
                ยืนยัน
            </button>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
  submitForm() {
    window.location.href = '/home/Finishpay';
  }
}
}
</script>

<style>

</style>