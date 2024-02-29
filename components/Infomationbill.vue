<template>
    <div class="font-bold text-3xl mt-7 ml-44">
        <p>รายละเอียดและรายชื่อของผู้เช่า</p>
    </div>
    <div class="bg-white mt-5">
        <div class='relative max-w-md mx-auto drop-shadow-md'>
            <input type="text" placeholder="ค้นหา" class="pl-10 pr-4 py-2 rounded-lg border border-gray-300 w-full">
            <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none">
                <svg class="h-5 w-5 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 10-14 0 7 7 0 0014 0z" />
                </svg>
            </div>
        </div>    
    </div>
    <div class="font-bold text-xl mt-5 ml-44">
        ห้องทั้งหมด
    </div>
    <div class="flex justify-between bg-[#FFFFFF] h-[250px] ml-40 mr-40 mt-5 rounded-2xl drop-shadow-[0_35px_35px_rgba(0,0,0,0.10)]">
        <div class="">
            <p class="bg-blue-300 rounded-tl-2xl rounded-br-3xl px-6 text-2xl font-bold">A101</p>
        </div>
        <div class="flex items-center">
            <img src="../public/nadeach.jpg" class="rounded-full h-[150px] w-[150px] border-blue-500 border-8">
         </div>
         <div class="grid grid-cols-2 items-center pl-10">
            <div class="flex items-center">
                <i class="fa-solid fa-user pr-2"></i>
                <p class="pr-3">ชื่อ ณเดชน์     คลูชิมิจ๊ะ</p>
            </div>
            <div class="flex items-center">
                <i class="fa-regular fa-user pr-2"></i>
                <p>ชื่อเล่น บาส</p>
            </div>
            <div class="flex items-center">
                <i class="fa-solid fa-mobile-screen-button pr-2"></i>
                <p>เบอร์ 099-999-9999</p>
            </div>
            <div class="flex items-center">
                <i class="fa-solid fa-envelope pr-2"></i>
                <p>อีเมล Nadacheiei@gimi.com</p>
            </div>
            <div class="flex items-center">
                <i class="fa-solid fa-file-signature pr-2"></i>
                <p>เริ่มทำสัญญา 14 มกราคม 2541</p>
            </div>
         </div>
        <div class="flex flex-col justify-between">
            <div class="mt-5">
                <div>
                    <p class="bg-[#56F000] mb-3 px-7 rounded-l-lg font-bold flex justify-center">สถานะ: กำลังเช่า</p>
                </div>
                <div class="flex justify-end">
                    <button class="flex items-center justify-center bg-[#A7CAFF] hover:bg-[#6E9FE8] ml-20 rounded-l-lg">
                        <p class="px-3 font-bold">แชต</p>
                        <i class="fa-solid fa-comment pr-3"></i>
                    </button>
                </div>
            </div>
            <div class="mb-2">
                <a href="/owner/Tanant in formation" class="text-[#3D9DD9] hover:underline flex justify-center">รายละเอียดเพิ่มเติม...</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style>

</style>