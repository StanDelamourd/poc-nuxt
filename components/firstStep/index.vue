<template>
  <div>
    <h1>S'inscrire</h1>
    <Field :value="name" label="Nom"/>
    <Field :value="firstname" label="Prenom"/>
  </div>
</template>

<script>
import Field from '../field';
export default {
  name: 'firstStep',
  components: {
    Field
  },
  data(){
    return {
      name: '',
      firstname: ''
    };
  }
}
</script>
<style scoped>

</style>