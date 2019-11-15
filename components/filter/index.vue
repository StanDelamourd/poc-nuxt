<template>
  <select>
    <option v-for="data in datas" :key="data.value" :value="data.value">{{data.value}}</option>
  </select>
</template>
<script>
export default {
  name: 'FilterSelect',
  props: {
    datas: {
      type: Array,
      required: true
    }
  }
}
</script>
<style scoped>
  select {
    background:transparent;
    background-image: url("data:image/svg+xml;utf8,<svg fill='black' height='24' viewBox='0 0 24 24' width='24' xmlns='http://www.w3.org/2000/svg'><path d='M7 10l5 5 5-5z'/><path d='M0 0h24v24H0z' fill='none'/></svg>");
    background-repeat: no-repeat;
    background-position-x: 100%;
    background-position-y: 5px;
    display: inline-block;
    color: black;
    border: 1px solid black;
    height: 5vh;
    margin-top: 1vh;
    margin-right: 5vw;
    padding-left: 10px;
    padding-right: 30px;
    border-radius: 12px;
  }
  option {
    color: black;
  }
</style>