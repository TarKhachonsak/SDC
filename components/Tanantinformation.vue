<template>
  <div class="flex justify-center">
    <div class="">
        <div class="border-4 border-[#3D9DD9] my-20">
            <div class="w-full">
                <p class="bg-[#3D9DD9] text-white text-2xl font-bold px-5 py-2">รายละเอียดของผู้เช่า</p>
            </div>
            <div class="px-10 pt-10">
                <img src="../public/nadeach.jpg" class="h-24 w-24 rounded-full">
            </div>
            <div class="grid grid-cols-3 mx-44 pb-5">
                <div class="my-5 ">
                    <p class="text-xl font-bold py-2">ชื่อจริง</p>
                    <p>นาย ณเดชน์</p>
                </div>
                <div class="my-5 mx-10">
                    <p class="text-xl font-bold py-2">นามสกุล</p>
                    <p>คลูชิมิจ๊ะ</p>
                </div>
                <div class="my-5 mx-10">
                    <p class="text-xl font-bold py-2">ชื่อเล่น</p>
                    <p>บาส</p>
                </div>
                <div class="my-5">
                    <p class="text-xl font-bold py-2">เบอร์</p>
                    <p>099-999-9999</p>
                </div>
                <div class="my-5 mx-10">
                    <p class="text-xl font-bold py-2">อีเมล</p>
                    <p>Nadacheiei@gimi.com</p>
                </div>
                <div class="my-5 mx-10">
                    <p class="text-xl font-bold py-2">วันเดือนปีเกิด</p>
                    <p>19/01/67</p>
                </div>
                <div class="my-5">
                    <p class="text-xl font-bold py-2">หมายเลขบัตรประชาชน</p>
                    <p>15888001235612</p>
                </div>
                <div class="my-5 mx-10">
                    <p class="text-xl font-bold py-2">หมายเลขห้องพัก</p>
                    <p>A101</p>
                </div>
            </div>
            <div class="mx-44 my-5">
                <p class="text-xl font-bold py-2">ที่อยู่ภูมิลำเนา</p>
                <p>123 หมู่ 99 บ้าน xxx ตำบล xxx อำเภอ xxx จังหวัด xxx 57123</p>
            </div>
            <div class="mx-44 my-10">
                <p class="text-xl font-bold py-2">สำเนาบัตรประชาชน</p>
                <img src="../public/card.png" alt="" class="mr-32 mb-10 w-[500px]">
            </div>
            <div @click="submitForm" class="mx-4 my-4 justify-end flex">
            <button class="bg-[#0075BE] hover:bg-[#005B94] text-white text-xl px-28 py-2 rounded-full">อัปโหลดบิล</button>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
  submitForm() {
    window.location.href = '/owner/Upload';
  }
}
}
</script>