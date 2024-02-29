<template>
  <div class="alert-box" :style="{ backgroundColor: boxColor }">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'AlertBox',
  props: {
    boxColor: {
      type: String,
      default: '#ffffff' // สีเริ่มต้นของกล่อง
    }
  }
}
</script>

<style scoped>
.alert-box {
  border: 1px solid #ccc;
  padding: 50px; 
  margin: 100px; 
}

</style>