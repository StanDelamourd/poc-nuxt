<template>
  <button @click="clickEvent">{{title}}</button>
</template>
<script>
export default {
  name: 'Button',
  props: {
    title: {
      required: true,
      type: String
    },
    clickEvent: {
      required: false,
      type: Function
    }
  }  
}
</script>
<style scoped>
button {
  display: block;
  background: #000;
  padding: 15px;
  width: 100%;
  color: white;
  margin-top: 1vh;
}
</style>