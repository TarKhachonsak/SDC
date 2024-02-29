<template>
  <HeaderL />
  <Banner class="h-screen" />
  <div class="grid gap-4 grid-cols-2 h-screen bg-indigo-100">
    <div class="">space</div>
    <div class="h-auto w-auto px-[200px] pt-[200px] items-center">
      <div class="border-box p-4 bg-slate-50 rounded shadow-lg">
        <h2 class="text-center text-2xl font-bold">ลืมรหัสผ่าน</h2>
        <div class="mt-3 mb-1">
          <label for="email"
            ><span>โปรดกรอกอีเมลของคุณ</span>
            <input
              type="email"
              name="email"
              id="email"
              v-model="field1"
              placeholder="Example@SDC.co.th"
              class="mt-2 block w-full rounded-md border-0 py-1.5 pl-2 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-400 sm:text-sm sm:leading-6 invalid:[&:not(:placeholder-shown):not(:focus)]:border-red-500 peer"
              required
              pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$"
            />
            <span
              class="mt-2 hidden text-sm text-red-500 peer-[&:not(:placeholder-shown):not(:focus):invalid]:block"
            >
              โปรดใส่อีเมลที่ถูกต้อง
            </span>
          </label>
        </div>
        <form @submit.prevent="submitForm">
          <div class="mt-3 mb-2">
            <button
              type="submit"
              :class="{
                'cursor-not-allowed': isFormInvalid,
                'hover:bg-sky-600 bg-sky-500': !isFormInvalid,
              }"
              class="btn btn-info px-[14px] py-2 w-full items-center bg-sky-300 border rounded text-white"
              :disabled="isFormInvalid"
            >
              ยืนยัน
            </button>
          </div>
          <p class="text-center text-xs">
            มีบัญชีผู้ใช้งานหรือไม่?
            <a
              href="register"
              class="text-blue-500 text-xs no-underline hover:underline"
            >
              สร้างบัญชีผู้ใช้งาน</a
            >
          </p>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      field1: "",
      password: "",
    };
  },
  computed: {
    isFormInvalid() {
      const isField1Invalid = !this.isValidEmail(this.field1);

      return isField1Invalid;
    },
  },
  methods: {
    isValidEmail(email) {
      const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      return emailRegex.test(email);
    },
    submitForm() {
      window.location.href = "/user/forgotpasswordfin";
    },
  },
};
</script>