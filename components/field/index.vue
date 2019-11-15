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
    <input v-else :type="inputType || 'text'" @input="updateValue($event.target.value)"/>
  </div>
</template>

<script>
export default {
  name: 'Field',
  props: {
    inputType: {
      type: String,
      default: 'text',
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
  created(){
    console.log(this.disabled);
  },
  methods:{
    updateValue(inputValue){
      this.$emit('value', inputValue)
    }
  }
}
</script>
<style scoped>
  label{
    font-family: 'Telegraf';
    font-weight: 800;
    color: #868686;
  }
  input[type=range]{
    width: 100%;
  }
  input[type=range]::-webkit-slider-thumb {
    background: #000;
    border: 1px solid black;
  }
  input[type=range]::-moz-range-thumb {
    background: #000;
    border: 1px solid black;
  }
  input[type=range]::-webkit-slider-runnable-track {
    background: #000;
    border: 1px solid black;
  }

  input[type=range]:focus::-webkit-slider-runnable-track {
    background: #000;
  }

input[type=range]::-moz-range-track {
  width: 100%;
  height: 1px;
  cursor: pointer;
  box-shadow: 1px 1px 1px #000000, 0px 0px 1px #0d0d0d;
  background: #000;
}
  input[type=range]::-ms-track {
    width: 100%;
    height: 1px;
    cursor: pointer;
    box-shadow: 1px 1px 1px #000000, 0px 0px 1px #0d0d0d;
    background: #000;
  }
  input[type=range]::-ms-fill-lower {
    background: #000;
    border: 0.2px solid #010101;
    box-shadow: 1px 1px 1px #000000, 0px 0px 1px #0d0d0d;
  }
  input[type=range]:focus::-ms-fill-lower {
    background: #000;
  }
  input[type=range]::-ms-fill-upper {
    background: #000;
    border: 0.2px solid #010101;
    box-shadow: 1px 1px 1px #000000, 0px 0px 1px #0d0d0d;
  }
  input[type=range]:focus::-ms-fill-upper {
    background: #000;
    height: 1vh;
  }

  .form__range{
    display: flex;
    justify-content: space-between;  
  }
  select{
    background-image: url("data:image/svg+xml;utf8,<svg fill='black' height='24' viewBox='0 0 24 24' width='24' xmlns='http://www.w3.org/2000/svg'><path d='M7 10l5 5 5-5z'/><path d='M0 0h24v24H0z' fill='none'/></svg>");
    background-repeat: no-repeat;
    background-position-x: 100%;
    background-position-y: 5px;
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
    border-bottom: 1px solid black;
    height: 5vh;
    margin-top: 1vh;
  }
</style>