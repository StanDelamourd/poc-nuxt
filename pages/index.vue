<template>
  <div>
    <img src="icon.png" alt="logo">
    <div class="home__button">
      <Button title="S'inscrire"/>
      <Button title="Se connecter" :clickEvent="this.test"/>
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
      this.$router.push({name: 'inscription'})
    }
  }
}
</script>
<style scoped>
img {
  width: 50%;
  margin: 20vh auto 0 auto;
  display: block;
}
.home__button{
  margin-top: 25vh;
}
</style>