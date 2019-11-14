<template>
  <div class="formGroup">
    <label for="">{{label}}</label>
    <select v-if="datas" name="" id="" @change="updateValue($event.target.value)">
      <option v-for="data in datas" :key="data.value" :value="data.title">{{data.title}}</option>
    </select>
    <div v-else-if="inputType === 'range'">
      <div class="form__range">
        <p>0</p>
        <p>Illimite</p>
      </div>
      <input type="range" @input="updateValue($event.target.value)">
    </div>
    <input v-else :type="inputType || 'text'" @input="updateValue($event.target.value)" :disabled="disabled || false"/>
  </div>
</template>

<script>
export default {
  name: 'Field',
  props: {
    disabled:{
      type: Boolean,
    },
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
  input[type=range]{
    width: 100%;
  }
  input[type=range]::-ms-track {
    background: #000;
    width: 100%;
    border: 1px solid black;
  }
  input[type=range]::-webkit-slider-thumb {
    background: #000;
    border: 1px solid black;
  }
  input[type=range]::-moz-range-thumb {
    background: #000;
    border: 1px solid black;
  }
  .form__range{
    display: flex;
    justify-content: space-between;  
  }
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
  input[type=text], input[type=password], input[type=email] {
    width: 100%;
    border: 1px solid black;
    height: 5vh;
    margin-top: 1vh;
  }
</style>