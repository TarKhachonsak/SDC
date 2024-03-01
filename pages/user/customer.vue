<template>
  <HeaderL />
  <Banner class="h-screen" />
  <div>
    <div class="grid gap-4 grid-cols-2 h-screen bg-indigo-100">
      <div class="">space</div>
      <div class="h-auto w-auto px-[50px] pt-[110px] items-center">
        <div class="border-box p-4 bg-slate-50 rounded shadow-lg">
          <h2 class="text-center text-2xl font-bold mb-4 col-span-2">
            สร้างบัญชีผู้ใช้งาน
          </h2>
          <label for="name">
            ชื่อ
            <input
              type="text"
              name="name"
              id="name"
              v-model="name"
              placeholder=""
              class="block w-full rounded-md border-0 py-1.5 pl-2 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-400 sm:text-sm sm:leading-6 invalid:[&:not(:placeholder-shown):not(:focus)]:border-red-500 peer"
              required
              pattern="[ก-๙]+( [ก-๙]+)?"
            />
            <span
              class="mt-2 hidden text-sm text-red-500 peer-[&:not(:placeholder-shown):not(:focus):invalid]:block"
            >
              โปรดกรอกด้วยภาษาไทย
            </span>
          </label>
          <label for="surname">
            <span>นามสกุล </span>
            <input
              type="text"
              name="surname"
              id="surname"
              v-model="surname"
              placeholder=""
              class="block w-full rounded-md border-0 py-1.5 pl-2 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-400 sm:text-sm sm:leading-6 invalid:[&:not(:placeholder-shown):not(:focus)]:border-red-500 peer"
              required
              pattern="[ก-๙]+( [ก-๙]+)?"
            />
            <span
              class="mt-2 hidden text-sm text-red-500 peer-[&:not(:placeholder-shown):not(:focus):invalid]:block"
            >
              โปรดกรอกด้วยภาษาไทย
            </span>
          </label>
          <label for="email">
            <span>อีเมล</span>
            <input
              type="email"
              name="email"
              id="email"
              v-model="email"
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
          <label for="password" class="col-start-1 col-end-2">
            <span>สร้างรหัสผ่าน </span>
            <input
              type="password"
              name="password"
              id="password"
              v-model="password"
              placeholder=""
              class="block w-full rounded-md border-0 py-1.5 pl-2 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-400 sm:text-sm sm:leading-6"
              @input="checkPasswordLength"
            />
            <div>
              <span v-if="showAdvice" class="text-red-500"
                >กรุณาใส่รหัสผ่านที่มีความยาวอย่างน้อย 8 ตัว</span
              >
            </div>
          </label>
          <label for="Cpassword" class="col-start-1 col-end-2">
            <span>ยืนยันรหัสผ่าน</span>
            <input
              type="password"
              name="Cpassword"
              id="Cpassword"
              v-model="Cpassword"
              placeholder=""
              class="block w-full rounded-md border-0 py-1.5 pl-2 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-400 sm:text-sm sm:leading-6 invalid:[&:not(:placeholder-shown):not(:focus)]:border-red-500 "

            />
       
          </label>
          <div class="mt-2 mb-2 col-start-1 col-end-3">
            <button
              @click="submitForm"
              type="submit"
              :class="{
                ' cursor-not-allowed': isFormInvalid,
                'hover:bg-sky-600 bg-sky-500': !isFormInvalid,
              }"
              :disabled="isFormInvalid"
              class="btn btn-info px-[14px] py-2 w-full items-center bg-sky-300 border rounded text-white"
            >
              ยืนยัน
            </button>
            <p class="text-center text-xs mt-4">
              มีบัญชีผู้ใช้งานแล้ว?
              <a
                href="login"
                class="text-blue-500 text-xs no-underline hover:underline"
                >เข้าสู่ระบบ</a
              >
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedPrefix: "",
      prefixes: ["นาย", "นาง", "นางสาว"],
      password: "",
      Cpassword: "",
      name: "",
      surname: "",
      email: "",
      showAdvice: true,
    };
  },
  computed: {
    isFormInvalid() {
      const isField1Invalid = !this.isValidEmail(this.email);
      const isField2Invalid = this.password.length < 7;
      const isField3Invalid =
        !this.isValidName(this.name) || this.name.length < 1;
      const isField4Invalid =
        !this.isValidSurname(this.surname) || this.name.length < 1;
      const isField5Invalid = this.Cpassword.length < 1;
      const isFieldsMatch = this.password === this.CPassword;

      console.log("isEmailInvalid:", isField1Invalid);
      console.log("isPasswordInvalid:", isField2Invalid);
      console.log("isNameInvalid:", isField3Invalid);
      console.log("isSurNameInvalid:", isField4Invalid);
      console.log("isConfirm,Invalid:", isField5Invalid);
      console.log("isFieldsMatch:", isFieldsMatch);
      console.log("   ");

      return (
        isField1Invalid ||
        isField2Invalid ||
        isField3Invalid ||
        isField4Invalid ||
        isField5Invalid ||
        isFieldsMatch
      );
    },
  },
  methods: {
    submitForm() {
      if (this.password !== this.Cpassword) {
        alert("รหัสผ่านที่ยืนยันไม่ตรงกัน");
        return;
      } else {
        console.log("รหัสผ่านถูกต้อง");
        // ถ้ามีความยาวมากกว่าหรือเท่ากับ 8 ตัว
        window.location.href = "/user/confirmR-C";
      }
    },
    isValidEmail(email) {
      const emailRegex = /^[^\s@]+@[^\s@]+\.[a-z]{2,}$/;
      return emailRegex.test(email);
    },
    isValidName(name) {
      const thaiPattern = /[ก-๙]/;
      return thaiPattern.test(name);
    },
    isValidSurname(surname) {
      const thaiPattern = /[ก-๙]/;
      return thaiPattern.test(surname);
    },
    checkPasswordLength() {
      this.showAdvice = this.password.length < 8;
    },
  },
};
</script>