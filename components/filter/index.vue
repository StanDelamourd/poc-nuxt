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
select{
    background:#fff;
    color: black;
    border: 1px solid black;
    height: 5vh;
    margin-top: 1vh;
    padding-left: 10px;
  }
  option {
    color: black;
  }
</style>