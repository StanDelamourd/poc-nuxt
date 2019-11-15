<template>
  <div>
    <img src="logo.png" alt="logo">
    <div class="home__button">
      <Button title="S'inscrire" :clickEvent="this.test"/>
      <Button title="Se connecter"/>
    </div>
  </div>
</template>

<script>
import Button from '../components/button';
export default {
  components: {
    Button
  },
  methods:{
    test() {
      this.$router.push({name: 'register'})
    }
  }
}
</script>
<style scoped>
img {
  width: 90%;
  margin: 20vh auto 0 auto;
  display: block;
}
.home__button{
  margin-top: 25vh;
}
</style>