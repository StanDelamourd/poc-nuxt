<template>
  <div>
    <h1>Metier</h1>
    <h2>Dans quel type de metier aimeriez-vous travailler ?</h2>
    <Field :value="situation" label="Situation" :datas="situations"/>
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
      situation: '',
      situations: [
        {
          title: 'Chomage'
        },
        {
          title: 'Sans emploi'
        }
      ]
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
  margin-bottom: 10vh;
}
</style>