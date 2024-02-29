<template>
<Navbar/>
  <div class="container">
    <div class="post">
        <h2>
            หอพักAAกว้างไหมคะ
        </h2>
        <img src="public/room.jpg" width="700" height="700">
        <p>อยากทราบว่าหอพักAAห้องกว้างมั้ยคะสามารถทำกับข้าวได้ไหมคะ                    เราอยู่2คนกับเพื่อนค่ะ แล้วหอพักเป็นอย่างไรบ้างค่าน้ำค่าไฟแพงมั้ย ตกอยู่เดือนประมาณกี่บาท อยาก                      ทราบประมาณนี้ค่ะขอบคุณค่ะ</p>
    </div>
    <div class="post" v-for="(post, index) in posts" :key="index">
      <p>{{ post.content }}</p>
    </div>
    <button class="btn-create" @click="goToCreatePage">+ ตั้งกระทู้</button>
  </div>
  <Footer/>
</template>

<script>
export default {
  data() {
    return {
      posts: [
        { content: 'ตอนนี้ได้ย้ายมาอยู่หรือยังครับผมอยู่ที่นี่มาปีกว่าละเผื่อใครมาอ่านทีหลังแล้วอยากรู้ข้อมูลเพิ่มเติมหลังไมค์                      มาได้ครับ'},
        { content: 'หอพักที่นี้สามารถเลี้ยงแมวได้ครับ'},
        { content: 'หอนี้สะอาดมากครับ'},
        { content: 'ถ้าเป็นห้องเดี่ยวจะเป็นประมาณนี้ค่ะ สามารถทำอาหารได้ค่ะ ค่าไฟหน่วยละ 8 บาท แต่เราไม่รู้ว่าห้อง                      สองคนเป็นยังไง เราว่าน่าจะใหญ่กว่าในรูปนะคะ', imageUrl: 'data:image/jpeg;base64,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' }
      ]
    };
  },
  methods: {
    goToCreatePage() {
      window.location.href = '/home/create_box';
    }
  }
};
</script>

<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.post {
  background-color: #D9E8F5;
  padding: 10px;
  margin-bottom: 30px;
  border-radius: 5px;
  box-shadow: 10px 8px 5px #8888;
}

.btn-create {
  position: absolute;
  top: 100px;
  right: 20px;
  background-color: #0075BE;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
</style>