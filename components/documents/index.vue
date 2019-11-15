<template>
  <div>
    <ul>
      <li>CV</li>
      <li>Diplome</li>
    </ul>
    <Button title="Ajouter mes pieces"/>
  </div>
</template>

<script>
import Button from '../button';
export default {
  name: 'documents',
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