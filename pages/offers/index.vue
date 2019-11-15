<template>
  <div class="offers__content">
    <div v-if="disable === false" class="complete">
      <img @click="disableComplete" src="Cross.png" alt="cross">
      <p>Completez votre profil avec votre diplome et votre CV pour acceder aux offres d'emplois</p>
    </div>
    <div class="filters">
      <input type="search">
      <div class="filters__select">
        <FilterSelect :datas="times" />
        <FilterSelect :datas="missions" />
        <FilterSelect :datas="interests" />
      </div>
    </div>
    <p class="title__offer">{{offers.length}} offres d'emplois</p>
    <div class="offers">
      <Offer v-for="offer in offers" :key="offer.profession" :offer="offer"/>
    </div>
  </div>
</template>

<script>
import Button from '../../components/button';
import FilterSelect from '../../components/filter';
import Offer from '../../components/offer';

export default {
  layout: 'profile',
  components:{
    Button,
    FilterSelect,
    Offer
  },
  data(){
    return {
      disable: false,
      times:[
        {
          value: 'Horaires'
        },
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
      interests:[
        {
          value: 'Champs d\'interets'
        },
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
          value: 'Missions'
        },
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
          profession: 'Auxiliaire de vie',
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
  },
  methods:{
    disableComplete(){
      this.disable = true;
    }
  }
}
</script>

<style scoped>
  .title__offer{
    padding-top: 20px;
    text-align: center;
  }
  .filters{
    border-bottom: 1px solid grey;
    padding-bottom: 10px; 
  }
  .filters__select{
    overflow-y: scroll;
    width: 100%;
  }
  .offers__content {
   width: 92%;
   height: 90vh;
   margin: auto; 
  }
  .complete{
    position: relative;
    margin-top: 2vh;
    width: 100%;
    padding: 15px;
    background: #FD5C63;
    border-radius: 5px; 
    color: #fff;
    font-weight: 800;
  }
  .complete img {
    height: 15px;
    width: 15px;
    position: absolute;
    top: 5px;
    right: 5px; 
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