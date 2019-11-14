<template>
  <div>
    <h1>Situation</h1>
    <h2>Pour que nous vous proposions des emplois adapte a votre besoin</h2>
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