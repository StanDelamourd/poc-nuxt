<template>
  <div class="card__offer" @click="$router.push({ name: 'offer'})">
    <img src="icon.png" alt="check"/>
    <div class="informations">
      <h3>{{offer.profession}}</h3>
      <p class="place">{{offer.place}}</p>
      <p>{{offer.type}} {{offer.time}}</p>
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
  .place {
    padding-bottom: 2vh;
  }
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
    margin-left: 2vw;
    height: 80px;
  }
  h3 {
    font-size: 1.5em;
    font-weight: 400;
  }
  .card__offer{
    position:relative;
    display: flex;
    padding: 10px;
    box-sizing: border-box;
    width: 100%;
    height: 19vh;
    margin-top: 2vh;
    box-shadow: 0 1px 4px rgba(125,125,125,.3);;
  }
</style>