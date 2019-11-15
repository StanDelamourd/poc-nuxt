<template>
  <div class="card__offer" @click="$router.push({ name: 'offer'})">
    <div class="card__infos">
      <img src="icon.png" alt="check"/>
      <div class="informations">
        <h3>{{offer.profession}}</h3>
        <p class="place">{{offer.place}}</p>
        <p>{{offer.type}} {{offer.time}}</p>
      </div>
    </div>
    <div class="popup">
      <p>Completez votre profil pour acceder a cette offre</p>
    </div>
  </div>  
</template>

<script>
export default {
  name: "offer",
  props:{
    offer: {
      type: Object,
      required: true
    }
  }
}
</script>>

<style scoped>
  .popup{
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 10px;
    background: rgba(125, 125, 125, .5);
    text-align:center;
    font-size: .8em;
  }
  img {
    border: 1px solid black;
    height: 80px;
  }
  .informations {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-left: 2vw;
    height: 80px;
  }
  .informations p {
    color: #7a7a7a;
  }
  h3 {
    font-family: 'Telegraf';
    font-size: 1.5em;
    font-weight: 800;
  }
  .card__infos{
    display: flex;
    align-items: center;
  }
  .card__offer{ 
    position:relative;
    padding: 10px;
    box-sizing: border-box;
    width: 100%;
    height: 19vh;
    margin-top: 2vh;
    box-shadow: 0 1px 4px rgba(125,125,125,.3);;
  }
</style>