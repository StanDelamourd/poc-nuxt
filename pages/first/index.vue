<template>
  <div>
    <div class="register__bg">
      <h1>S'inscrire</h1>
    </div>
    <div class="form">
      <form>
        <Field label="Email" inputType="email" />
        <Field label="Mot de passe" inputType="password" />
        <Field label="Confirmer mot de passe" inputType="password" />
      </form>
    </div>
    <button class="register__button" @click="$router.push({ name: 'register'})">S'inscrire</button>
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
  .form{
    border-radius: 40px;
    background: #fff;
    margin-top: -50px;
    padding-top: 50px;
  }
  button:last-child {
    width: 100%;
    margin: auto;
    margin-top: 3vh;
  }
  form {
    width: 80%;
    margin: auto;
  }
  .register__button {
    display: block;
    color: white;
    width: 90%;
    margin: auto;
    padding: 20px 0;
    background: #FD5C63;
    border-radius: 20px;
  }
  .register__bg{
    background: url('../../static/bg.png');
    height: 50vh;
  }
  .register__bg h1 {
    color: white;
    text-align:center;
    padding-top: 35vh;
    font-size: 2.4em;
  }
</style>