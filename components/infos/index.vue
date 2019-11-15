<template>
  <div>
    <ul>
      <li>Metier</li>
      <li>Ville</li>
      <li>Coordonnees</li>
      <li>Permis</li>
      <li>Vehicule</li>
    </ul>
    <Button label="Completez mes infos"/>
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
</style>