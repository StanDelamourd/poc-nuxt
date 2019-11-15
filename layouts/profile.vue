<template>
  <div>
    <div class="content">
      <nuxt/>
    </div>
    <nav>
      <ul>
        <li @click="$router.push({name: 'offers'})">Offres</li>
        <li @click="$router.push({name: 'profile'})">Profil</li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
}
</script>

<style scoped>
  * {
    font-family: 'Roboto'
  }
  .content {
    position: fixed;
    overflow: scroll;
    height: 90vh;
    padding-bottom: 2vh;
  }
  nav{
    position: fixed;
    height: 10vh;
    width: 100%;
    background: grey;
    bottom:0;
  }
  nav ul {
    display: flex;
    list-style: none;
  }
  nav ul li {
    width: 25%;
    color: white;
    text-align: center;
    line-height: 10vh;
  }
</style>