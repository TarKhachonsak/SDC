<template>
    <Navbarown/>
<div class="h-screen flex-col items-center mt-6 flex">
    <div class="align-middle w-1/3 mt-4">
    <label
            ><span>ค่าห้อง</span>
            <input
              
              class="block w-full rounded-md border-0 py-1.5 pl-2 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
            />
          </label>
    </div>
    <div class="w-1/3 mt-4">
    <label
            ><span>ค่าไฟ</span>
            <input
              
              class="block w-full rounded-md border-0 py-1.5 pl-2 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
            />
          </label>
    </div>
    <div class="w-1/3 mt-4">
    <label
            ><span>ค่าน้ำ</span>
            <input
              
              class="block w-full rounded-md border-0 py-1.5 pl-2 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
            />
          </label>
    </div>
    <div class="w-1/3 mt-4">
    <label
            ><span>ค่าอื่น ๆ โปรดระบุ</span>
            <input
              placeholder="ชื่อรายการ"
              class="block w-full rounded-md border-0 py-1.5 pl-2 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
            /><input
              placeholder="จำนวนที่ต้องจ่าย"
              class="mt-4 block w-full rounded-md border-0 py-1.5 pl-2 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
            />
          </label>
    </div>
            <div @click="submitForm" class="mt-5">
            <button class="bg-[#0075BE] hover:bg-[#005B94] text-white text-xl px-28 py-2 rounded-full">เสร็จสิ้น</button>
        </div>
</div>
    <Footerown/>
</template>

<script>
export default {
  methods: {
  submitForm() {
    window.location.href = '/owner/Tanant in formation';
  }
}
}
</script>
