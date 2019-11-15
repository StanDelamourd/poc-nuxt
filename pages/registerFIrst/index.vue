<template>
  <div>
    <div class="register__bg">
      <h1>S'inscrire</h1>
    </div>
    <div class="form">
      <form>
      </form>
    </div>
    <button class="register__button">S'inscrire</button>
    <button>Deja inscrit</button>
  </div>  
</template>

<script>
import Button from '../../components/button';
import Field from '../../components/field';
export default {
  data () {
    return {
      step: 1,
    }
  },
  components:{
    Field,
  },
  methods:{
    changeStep(){
      this.step += 1;
    }
  }
}
</script>

<style scoped>
  form {
    width: 100%;
  }
  .register__bg{
    background: url('../../static/bg.png');
  }
</style>