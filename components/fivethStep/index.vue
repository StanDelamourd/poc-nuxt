<template>
  <div>
    <h1>Ou habitez-vous ?</h1>
    <h2>Trouvez un job au plus proche de votre logement</h2>
    <Field :value="city" label="Ville"/>
    <Field :value="radius" inputType="range" label="Rayon"/>
  </div>
</template>

<script>
import Field from '../field';
export default {
  name: 'thirdStep',
  components: {
    Field
  },
  data(){
    return {
      city: '',
      radius: 1
    };
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
</style>