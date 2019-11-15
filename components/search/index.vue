<template>
  <div>
    <ul>
      <li>Type de public</li>
      <li>Type de contrat</li>
      <li>Champs d'intervention</li>
    </ul>
    <Button title="Affiner ma recherche"/>
  </div>
</template>

<script>
import Button from '../button';
export default {
  name: 'search',
  components:{
    Button
  }
}
</script>

<style scoped>
  div{
    width: 90%;
    height: 35vh;
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