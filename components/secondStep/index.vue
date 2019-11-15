<template>
  <div>
    <h1>Bienvenue sur A2JOB</h1>
    <h2>Tu n'as plus qu'a renseigner quelques informations sur toi</h2>
    <Field :value="name" label="Nom"/>
    <Field :value="firstname" label="Prenom"/>
  </div>
</template>

<script>
import Field from '../field';
export default {
  name: 'SecondStep',
  components: {
    Field
  },
  data(){
    return {
      name: '',
      firstname: '',
    };
  }
}
</script>
<style scoped>
  h1 {
    font-size: 2.3em;
    margin-bottom:2vh;
  }
  h2 {
    font-size: 1.4em;
    font-weight: 400;
    color: #5C5C5C;
    margin-bottom:10vh; 
  }
</style>