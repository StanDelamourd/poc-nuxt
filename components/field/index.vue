<template>
  <div class="formGroup">
    <label for="">{{label}}</label>
    <input :type="inputType" @input="updateValue($event.target.value)"/>
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