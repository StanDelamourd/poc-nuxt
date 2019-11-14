<template>
  <div>
    <div class="form">
      <form>
        <FirstStep/>
      </form>
    </div>
    <Button title="Suivant" />
  </div>  
</template>
<script>
import FirstStep from '../../components/firstStep';
import Button from '../../components/button';

export default {
  data () {
    return {

    }
  },
  components:{
    FirstStep,
    Button
  }
}
</script>

<style scoped>
  div >>> button {
    position: absolute;
    left: 50%;
    bottom: 5vh;
    transform: translate(-50%, 0);
    width: 95%;
  }
  .form {
    height: 90vh;
    display: flex;
    align-items: center;
  }
  form {
    width: 100%;
  }
</style>