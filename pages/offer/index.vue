<template>
  <div class="offer">
    <div class="offer__title">
      <img src="icon.png" alt="Offer picture">
      <div>
        <h1>Infirmier</h1>
        <h2>EHPAD Bordeaux</h2>
        <h2>CDD 18 mois</h2>
      </div>
    </div>
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
    </div>
    <div class="description">
      <p>La Villa Danielle Torelli, EHPAD associative située dans le 15ème arrondissent de Paris, (80 résidents, dont une unité pilote pour jeunes patients Alzheimer et un PASA) recrute un infirmier pour travailler en journée.</p>
      <p> L'infirmier est chargé de la gestion des traitements des résidents, de la coordination des soins, de l'accompagnement et de la supervision de l'équipe. Sous l'autorité du cadre infirmier, il travaille en étroite collaboration avec le médecin coordonnateur et l'ensemble de l'équipe pluridisciplinaire</p>
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
  * {
    font-family: 'Telegraf'
  }
  .offer__title {
    display: flex;
    margin-top: 2vh;
  }
  .offer__title img {
    height: 80px;
    width: 80px;
  }
  .description{
    margin-top: 5vh;
  }
  .description p{
    margin-top: 2vh;
  }
  h3 {
    font-size: 1em;
    margin-top: 2vh;
    font-weight: 400;
  }
  .othersOffers{
    text-align: center;
    font-size: 2em;
  }
  h1{
    padding-top: 1.5vh;
    font-weight: 400;
    font-size: 1.4em;
  }
  h2{
    font-weight: 400;
    font-size: 1.2em;
  }
  h2:last-child{
    font-weight: 400;
    font-size: 1em;
  }
  .offer {
    width: 92% ;
    margin: auto;
    position: relative;
  }
  .offer__infos{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    font-size: .9em;
  }
  .offer__infos div {
    width: 33%;
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