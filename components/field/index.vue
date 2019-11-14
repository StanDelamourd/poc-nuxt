<template>
  <div class="formGroup">
    <label for="">{{label}}</label>
    <select v-if="datas" name="" id="" @change="updateValue($event.target.value)">
      <option v-for="data in datas" :key="data.value" :value="data.title">{{data.title}}</option>
    </select>
    <input v-else :type="inputType" @input="updateValue($event.target.value)"/>
  </div>
</template>

<script>
export default {
  name: 'Field',
  props: {
    inputType: {
      type: String,
      value: 'text',
    },
    datas: {
      type: Array,
    },
    label: {
      type: String,
      required: true,
    },
    value:{
      type: String,
      required: true
    }
  },
  methods:{
    updateValue(inputValue){
      this.$emit('value', inputValue)
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
  .formGroup{
    margin-bottom: 2vh;
  }
  label{
    display: block;
  }
  input {
    width: 100%;
    border: 1px solid black;
    height: 5vh;
    margin-top: 1vh;
  }
</style>