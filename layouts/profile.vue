<template>
  <div>
    <div class="content">
      <nuxt/>
    </div>
    <nav>
      <ul>
        <li @click="$router.push({name: 'offers'})"><img :src="$nuxt.$route.path === '/offers' ? 'offer-red.png' : 'offer.svg'" alt="offer"></li>
        <li><img src="message.png" alt="message"></li>
        <li><img src="bell.png" alt="offer"></li>
        <li @click="$router.push({name: 'profile'})"><img :src="$nuxt.$route.path === '/profile' ? 'user-red.png' : 'user.png'" alt="user"></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
}
</script>

<style scoped>
  @font-face {
    font-family: "Telegraf";
    src: url("/fonts/telegraf/Telegraf-Regular-200.otf") format("opentype");
    font-weight: 200;
  }
  @font-face {
    font-family: "Telegraf";
    src: url("/fonts/telegraf/Telegraf-Regular-400.otf") format("opentype");
    font-weight: 400;
  }
  @font-face {
    font-family: "Telegraf";
    src: url("/fonts/telegraf/Telegraf-Regular-800.otf") format("opentype");
    font-weight: 800;
  }
  * {
    font-family: 'Telegraf'
  }
  .content {
    position: fixed;
    overflow: scroll;
    height: 90vh;
    width: 100%;
    padding-bottom: 2vh;
  }
  nav{
    position: fixed;
    height: 10vh;
    width: 100%;
    background: #fff;
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
  img {
    height: 20px;
    width: 20px;
  }
</style>