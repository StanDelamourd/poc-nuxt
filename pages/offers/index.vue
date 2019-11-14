<template>
  <div>
    <div class="complete">
      <p>Completez votre profil avec votre diplome et votre CV pour acceder aux offres d'emplois</p>
      <Button title="Ajouter mes pieces"/>
    </div>
    <div class="filters">
      <input type="search">
      <div class="filters__select">
        <!-- <Filter :datas="times" />
        <Filter :datas="missions" /> -->
      </div>
    </div>
    <div class="offers">
      <Offer v-for="offer in offers" :key="offer.profession" :offer="offer"/>
    </div>
  </div>
</template>

<script>
import Button from '../../components/button';
import Filter from '../../components/filter';
import Offer from '../../components/offer';

export default {
  components:{
    Button,
    Filter,
    Offer
  },
  data(){
    return {
      times:[
        {
          value: '6 mois'
        },
        {
          value: '12 mois'
        },
        {
          value: '18 mois'
        },
        {
          value: '24 mois'
        }
      ],
      missions: [
        {
          value: 'Infirmier'
        },
        {
          value: 'Medecin'
        },
        {
          value: 'Educateur(rice)'
        }
      ],
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
        },
        {
          profession: 'Aide soignante',
          place: 'EHPAD, Bordeaux',
          type: 'CDD',
          time: '18 mois'
        },
        {
          profession: 'Auxiliaire de puericulture',
          place: 'EHPAD, Bordeaux',
          type: 'CDD',
          time: '18 mois'
        },
        {
          profession: 'Pharmacien',
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
  .complete{
    margin-top: 2vh;
    width: 100%;
    padding: 15px;
    background: rgba(125, 125, 125, .5);
    text-align: center; 
  }
  .complete p {
    padding-bottom: 2vh;
  }
  input {
    width: 100%;
    border: 1px solid black;
    height: 5vh;
    margin-top: 1vh;
  }
</style>