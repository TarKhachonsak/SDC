<template>
  <nav class="bg-white shadow-md">
    <div id="menu" class="flex justify-between items-center px-12">
        <div id="logo">
            <a href="/user/login"><img src="public/logo.png" class="size-20"></a>
        </div>
        <ul class="flex font-bold text-black ">
            <li class="hover:text-[#0075BE] p-3"><a href="/owner">หน้าแรก</a></li>
            <li class="hover:text-[#0075BE] p-3"><a href="/owner/Alltenantinfomation">ติดต่อ</a></li>
            <li class="hover:text-[#0075BE] p-3"><a href="/owner/Aboutus">เกี่ยวกับเรา</a></li>
        </ul>
        <div id="message-profile" class="flex justify-center">
            <div class="px-2 py-1 m-1 flex items-center justify-center hover:bg-slate-200">
                <a href="/owner/Alert" class=""><i class="fa-regular fa-envelope"></i></a>
            </div>
            <div class="px-2 py-1 m-1 flex items-center justify-center hover:bg-slate-200">
                <a href="/owner/Profile" class=""><i class="fa-regular fa-user"></i></a>
            </div>
        </div>
    </div>
  </nav>
</template>

<script>
export default {

}
</script>

<style scoped>

</style>