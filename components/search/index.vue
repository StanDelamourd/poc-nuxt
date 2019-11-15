<template>
  <div>
    <ul>
      <li>Type de public</li>
      <li>Type de contrat</li>
      <li>Champs d'intervention</li>
    </ul>
    <Button label="Affiner ma recherche"/>
  </div>
</template>

<script>
import Button from '../button';
export default {
  name: 'infos',
  components:{
    Button
  }
}
</script>

<style scoped>
  div{
    width: 90%;
    height: 40vh;
    margin: auto;
  }
  div >>> button {
    width: 90%;
    margin: auto;
  }
</style>