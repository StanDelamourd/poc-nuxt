<template>
  <div>
    <ul>
      <li>CV</li>
      <li>Diplome</li>
    </ul>
    <Button label="Ajouter mes pieces"/>
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
    margin: auto;
  }
</style>