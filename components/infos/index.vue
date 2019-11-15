<template>
  <div>
    <ul>
      <li>Metier</li>
      <li>Ville</li>
      <li>Coordonnees</li>
      <li>Permis</li>
      <li>Vehicule</li>
    </ul>
    <Button title="Completez mes infos"/>
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
    position: relative;
  }
  div >>> button {
    margin: auto;
    position: absolute;
    bottom:0;
  }
  ul li {
    list-style: none;
  }
</style>