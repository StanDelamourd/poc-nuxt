<template>
  <select>
    <option v-for="data in datas" :key="data.value" :value="data.value">{{data.value}}</option>
  </select>
</template>
<script>
export default {
  name: 'filter',
  props: {
    datas: {
      type: Array,
      required: true
    }
  }
}
</script>
<style scoped>
select{
    background: grey;
    color: black;
    width: 100%;
    height: 5vh;
    margin-top: 1vh;
  }
  option {
    color: black;
  }
</style>