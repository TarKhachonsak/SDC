<template>
<Navbarown/>
<div class="h-screen items-center flex">
  <div class="container">
    <div class="form-group">
      <label for="title">ระบุคำถามของคุณ</label>
      <input type="text" id="title" v-model="post.title">
    </div>
    <div class="form-group">
      <label for="details">เขียนรายละเอียดของคำถาม</label>
      <textarea id="details" rows="4" v-model="post.details"></textarea>
    </div>
    <div class="form-group">
      <label for="image">อัพโหลดรูป:</label>
      <input type="file" id="image" accept="image/*" @change="handleImageUpload">
    </div>
    <button class="btn-post" @click="submitPost">โพสต์กระทู้</button>
  </div>
</div>
  <Footerown/>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: '',
        details: '',
        image: null
      }
    };
  },
  methods: {
    handleImageUpload(event) {
      this.post.image = event.target.files[0];
    },
    submitPost() {
      console.log(this.post);
    }
  }
};
</script>

<style scoped>
.container {
  max-width: 600px;
  margin: 50px auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #D9E8F5;
}
.form-group {
  margin-bottom: 20px;
}
.form-group label {
  display: block;
  font-weight: bold;
}
.form-group input[type="text"],
.form-group textarea {
  width: 100%;
  padding: 10px;
  border-radius: 5px;
  border: 1px solid #ccc;
  box-sizing: border-box;
}
.btn-post {
  display: block;
  margin: 0 auto;
  padding: 10px 20px;
  background-color: #56F000;
  color: black;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
</style>