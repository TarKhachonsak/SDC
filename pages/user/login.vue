<template>
  <HeaderL />
  <Banner class="h-screen" />
  <div class="grid gap-4 grid-cols-2 h-screen bg-indigo-100">
    <div class="">space</div>
    <div class="h-auto w-auto px-[200px] pt-[200px] items-center">
      <div class="border-box p-4 bg-slate-50 rounded shadow-lg">
        <h2 class="text-center text-2xl font-bold">ลงชื่อเข้าใช้งาน</h2>
        <div class="mt-3 mb-1">
          <label for="email"
            ><span>อีเมล</span>
            <input
              type="email"
              name="email"
              id="email"
              v-model="field1"
              placeholder="Example@SDC.co.th"
              class="block w-full rounded-md border-0 py-1.5 pl-2 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-400 sm:text-sm sm:leading-6 invalid:[&:not(:placeholder-shown):not(:focus)]:border-red-500 peer"
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
          <label for="password"
            ><span>รหัสผ่าน</span>
            <input
              type="password"
              name="password"
              id="password"
              v-model="password"
              placeholder=" "
              class="block w-full rounded-md border-0 py-1.5 pl-2 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
            />
          </label>

          <div class="mt-2 mb-1"></div>
          <h3 class="mt-1 text-right">
            <a
              href="forgotpassword"
              class="text-blue-500 text-xs no-underline hover:underline"
              >ลืมรหัสผ่าน?</a
            >
          </h3>
          <div class="mt-2 mb-2">
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
      const isField2Invalid = !this.isValidField2(this.password);
      return isField1Invalid || isField2Invalid;
    },
  },
  methods: {
    isValidEmail(email) {
      const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      return emailRegex.test(email);
    },
    isValidField2(password) {
      const alphanumericRegex = /^[a-zA-Z0-9]+$/;
      return password.length > 0;
    },
    submitForm() {
      // ตรวจสอบว่ารหัสผ่านมีความยาวอย่างน้อย 8 ตัว
      if (this.password.length < 8) {
        // ถ้าไม่ถึง 8 ตัวให้แสดง Alert
        alert("รหัสผ่านไม่ถูกต้อง");
      } else {
        // ถ้ามีความยาวมากกว่าหรือเท่ากับ 8 ตัว
        window.location.href = "/home";
      }
    },
  },
};
</script>