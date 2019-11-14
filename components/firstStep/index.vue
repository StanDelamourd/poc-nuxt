<template>
  <div>
    <Field :value="name" label="Nom"/>
    <Field :value="name" label="Prenom"/>
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