<template>
  <div>
    <h1>Votre contrat</h1>
    <h2>Etes-vous un citoyen de l'Union Europeene ?</h2>
    <div class="answer">
      <Button title="oui" :semi="true" :clickEvent="handleButton"/>
      <Button title="non" :semi="true" :clickEvent="handleButton"/>
    </div>
    <h2>Si ce n'est pas le cas, qu'elle est le type de votre contrat de travail ?</h2>
    <Field :value="contract" label="Contrat"/>
  </div>
</template>

<script>
import Button from '../button';
import Field from '../field';

export default {
  name: 'sixthStep',
  components:{
    Button,
    Field
  },
  data(){
    return {
      contract: ''
    }
  },
  methods:{
    handleButton(e){
      console.log('yes')
    }
  }
}
</script>
<style scoped>
.answer{
  margin: 5vh 0;
}
h1, h2 {
  text-align: center;
  font-weight: 500;
}
h1 {
  font-size: 1.5em;
}
h2 {
  font-size: 1em;
  margin-top: 2vh;
}
</style>