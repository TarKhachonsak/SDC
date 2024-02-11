<template>
    <HeaderL />
    <Banner class="h-screen" />
    <div class="grid gap-4 grid-cols-2 h-screen bg-indigo-100">
        <div class="">space</div>
        <div class="h-auto w-auto px-[200px] pt-[200px] items-center">
            <div class="border-box p-4 bg-slate-50 rounded shadow-lg">
                <h2 class="text-center text-2xl font-bold">คุณคือ?</h2>
                <a href="customer"><ButtonL class="mt-10 px-[14px] py-2 w-full items-center bg-sky-500 border rounded text-white hover:bg-sky-600" title="ผู้เช่า"/></a>
                <a href="owner"><ButtonL class="mt-5 px-[14px] py-2 w-full items-center bg-sky-500 border rounded text-white hover:bg-sky-600 " title="เจ้าของหอพัก"/></a>
                <p class="text-center text-xs mt-10">
          มีบัญชีผู้ใช้งานแล้ว?
          <a href="login" class="text-blue-500 text-xs no-underline hover:underline">
            เข้าสู่ระบบ</a
          >
        </p>
            </div>
            
        </div>
        
    </div>
</template>