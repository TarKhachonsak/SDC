<template>
     <Navbar/>
    
  <div class="user-profile h-[80vh] mt-10 mx-auto">
  

    <!-- ข้อมูลพื้นฐาน -->
    <section>
      <h2><b>ข้อมูลพื้นฐาน</b></h2>
      <div>
        <p><strong>ชื่อ-สกุล:</strong> <span>{{ userProfile.name }}</span> </p>
      </div>
    </section>

    <!-- เพศ -->
    <section>
     
      <div>
        <p><strong>เพศ:</strong> {{ userProfile.gender }} </p>
      </div>
    </section>

    <!-- ข้อมูลติดต่อ -->
    <section>
     <div><b>ข้อมูลติดต่อ</b></div>
    
      <div>
        <p><strong>อีเมล:</strong> {{ userProfile.email }}</p>
        <p><strong>เบอร์โทร:</strong> {{ userProfile.phone }} </p>
        <p><strong>ที่อยู่:</strong> {{ userProfile.address || 'ไม่ระบุ' }} </p>
      </div>
    </section>



    <!-- ปุ่มยืนยัน -->
   
  
  </div>
 <Footer/>
</template>

<script>
export default {
  data() {
    return {
      userProfile: {
        name: 'นาย แสงศักดิ์ วิบวับ',
        gender: 'ชาย',
        email: 'AAAAAAAA@gmail.com',
        phone: '08XXXXXXXX',
        address: null // ถ้าไม่มีที่อยู่ให้เป็น null
      }
    };
  },
  methods: {
    editProfile() {
      // การจัดการเหตุการณ์เมื่อคลิกที่ปุ่ม
      console.log('ยืนยัน');
    }
  }
};

</script>

<style scoped>
.user-profile {
  font-family: Arial, sans-serif;

  max-width: 600px;
  padding: 10px;
}

section {
  margin-bottom: 30px;
}

h1 {
  text-align: center;
}

h2 {
  margin-bottom: 10px;
}

.bold {
  font-weight: bold;
}

.change-password {
  color: #56F000;
  cursor: pointer;
}

button {
  background-color: #007BFF;
  color: white;
  padding: 5px 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  
}

button:hover {
  background-color: #49f128;
}
.shad {
  background: linear-gradient(rgb(240, 240, 240), rgb(255, 255, 255)); /* Standard syntax */
  height: 20px;
}
.centered {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 10px; /* กำหนดความสูงของพื้นที่มองเห็น */
}
</style>
<!---->>