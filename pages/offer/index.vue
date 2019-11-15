<template>
  <div class="offer">
    <h1>Infirmier</h1>
    <h2>EHPAD Bordeaux</h2>
    <div class="offer__infos">
      <div class="schedule">
        <p>Horaires</p>
        <p>Nuit, mi-temps</p>
      </div>
      <div class="remuneration">
        <p>Remuneration</p>
        <p>160€ brut/jour</p>
      </div>
      <div class="mobility">
        <p>Mobilite</p>
        <p>Vehicule requis</p>
      </div>
      <div class="experience">
        <p>Experience</p>
        <p>Intermediaire</p>
      </div>
    </div>
    <h3 class="description">Description</h3>
    <div>
      <p>Champ d'action</p>
      <p>Hebergement, Alzheimer</p>
    </div>
    <h3 class="othersOffers">Offres similaires</h3>
    <div class="offers">
      <Offer v-for="offer in offers" :key="offer.profession" :offer="offer"/>
    </div>
  </div>
</template>

<script>
import Offer from '../../components/offer';
export default {
  layout: 'profile',
  components:{
    Offer
  },
  data(){
    return {
      offers: [
        {
          profession: 'Infirmier',
          place: 'EHPAD, Bordeaux',
          type: 'CDD',
          time: '18 mois'
        },
        {
          profession: 'Medecin',
          place: 'EHPAD, Bordeaux',
          type: 'CDD',
          time: '18 mois'
        },
        {
          profession: 'Aide soignant',
          place: 'EHPAD, Bordeaux',
          type: 'CDD',
          time: '18 mois'
        }
      ]
    }
  }
}
</script>

<style scoped>
  h3 {
    font-size: 1em;
    margin-top: 10vh;
  }
  .othersOffers{
    text-align: center;
    font-size: 2em;
  }
  h1, h2 {
    text-align: center;
  }
  h1{
    padding-top: 2vh;
    font-weight: 400;
  }
  h2{
    padding-top: 1vh;
    font-weight: 400;
    font-size: 1.3em;
    margin-bottom: 2vh;
  }
  .offer {
    width: 92% ;
    margin: auto;
    position: relative;
  }
  .offer__infos{
    display: flex;
    flex-wrap: wrap;
  }
  .offer__infos div {
    width: 50%;
    margin-top: 3vh;
    text-align: center;
  }
  .offer__infos div p:first-child {
    font-weight: 500;
  }
  div >>> button {
    margin: auto;
    position: absolute;
    bottom:0;
  }
  ul li {
    list-style: none;
  }
</style>