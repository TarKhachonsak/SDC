<template>
  <HeaderL />
  <Banner class="h-screen" />
  <div class="grid gap-4 grid-cols-2 h-screen bg-indigo-100">
    <div class="">space</div>
    <div class="h-auto w-auto px-[200px] pt-[200px] items-center">
      <div class="border-box p-4 bg-slate-50 rounded shadow-lg">
        <div class="items-center">
          <img
            src="/correct.png?url"
            class="object-cover items-center"
            alt=""
          />
        </div>
        <h3 class="text-center mt-1 text-2xl font-bold">
          การลงทะเบียนเสร็จสิ้น
        </h3>

        <button
          @click="submitForm"
          class="btn btn-info mt-2 px-[14px] py-2 w-full items-center bg-sky-500 hover:bg-sky-600 border rounded text-white"
        >
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
    window.location.href = '/user/login';
  }
}
}
</script>
