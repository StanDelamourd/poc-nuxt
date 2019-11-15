<template>
  <div>
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
  div {
    width: 90% ;
    margin: auto;
    position: relative;
  }
  .offer__infos{
    display: flex;
    flex-wrap: wrap;
  }
  .offer__infos div {
    width: 50%;
    margin-top: 2vh;
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