<template>
  <button @click="execute" :class="[semi ? 'semiButton' : 'fullButton']">{{title}}</button>
</template>
<script>
export default {
  name: 'Button',
  props: {
    title: {
      required: true,
      type: String
    },
    semi: {
      type: Boolean,
    },
    clickEvent: {
      required: false,
      type: Function
    }
  },
  methods: {
    execute(){
      if(this.clickEvent){
        this.clickEvent();
      }
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
  .semiButton {
    display: inline-block;
    width: 49%;
  }
</style>