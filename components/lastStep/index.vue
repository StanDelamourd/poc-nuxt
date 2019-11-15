<template>
  <div>
    <img src="check.svg" alt="check">
    <h1>Vous y etes presque</h1>
    <h2>Veuillez confirmer votre adresse mail pour pouvoir continuer</h2>
    <Button title="Envoyer" :clickEvent="pushRoute"/>
  </div>
</template>>

<script>
import Button from '../button';
export default {
  name:'LastStep',
  components: {
    Button
  },
  methods:{
    pushRoute(){
      this.$router.push({name: 'offers'})
    }
  }

}
</script>
<style scoped>
  h1, h2 {
    text-align: center;
    font-weight: 500;
  }
  h1 {
    font-size: 1.5em;
  }
  h2 {
    font-size: 1em;
    margin: 2vh 0 10vh 0;
  }
  img {
    width: 50%;
    margin: 20vh auto 4vh auto;
    display: block;
  }
</style>