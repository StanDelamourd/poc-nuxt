<template>
  <div>
    <div class="profile__picture">
      <div class="profile__picture_cover"/>
      <img src="profile.png" alt="profile">
      <h1>Christine Millot</h1>
      <h2>Bordeaux, France</h2>
      <h2>Infirmiere</h2>
    </div>
    <div class="profile__complete">
      <p>Augmentez vos chances de trouver un emploi en completant votre profil</p>
      <div class="profile__complete_progression">
        <div/>
        <div/>
        <div/>
      </div>
    </div>
    <div class="profile__nav">
      <button :class="[selectedItem === 'info' ? 'selectedButton' : '']" @click="changeItem('info')">Mes infos</button>
      <button :class="[selectedItem === 'document' ? 'selectedButton' : '']" @click="changeItem('document')">Documents</button>
      <button :class="[selectedItem === 'search' ? 'selectedButton' : '']" @click="changeItem('search')">Ma recherche</button>
    </div>
    <Infos v-if="selectedItem === 'info'"/>
    <Documents v-if="selectedItem === 'document'"/>
    <Search v-if="selectedItem === 'search'"/>
  </div>
</template>

<script>
import Search from '../../components/search';
import Infos from '../../components/infos';
import Documents from '../../components/documents';

export default {
  layout: 'profile',
  components:{
    Search,
    Infos,
    Documents
  },
  data(){
    return {
      selectedItem: 'info'
    }
  },
  methods:{
    changeItem(value){
      this.selectedItem = value;
    }
  }
}
</script>

<style scoped>
  h2 {
    font-family: 'Telegraf';
    font-size: 1.2em;
    font-weight: 400;
    text-align: center;
  }
  h2:last-child {
    margin-bottom: 2vh;
  }
  .profile__nav {
    width: 92%;
    margin: auto;
    margin-top: 2vh;
    display: flex;
  }
  .selectedButton{
    border-bottom: 2px solid black;
  }
  .profile__nav button {
    height: 5vh;
    width: calc(100%/3);
    text-align: center;
  }
  .profile__picture_cover {
    width: 100%;
    height: 10vh;
    background: grey;
  }
  .profile__complete{
    background: rgba(125, 125, 125, .2);
    width: 92%;
    margin: auto;
    padding: 15px;
    font-size: 1.2em;
  }
  .profile__complete_progression {
    display: flex;
    justify-content: space-between;
    margin-top: 1vh;
  }
  .profile__complete_progression div{
    height: 1.2vh;
    width: 32%;
    border-radius:5px;
    background: rgba(125, 125, 125, .7);
  }
  .profile__complete_progression div:first-child {
    background: #000;
  }
  h1 {
    font-weight: 400;
    margin-top: 2vh;
    font-size: 1.5em;
  }
  img[alt=profile]{
    display: block;
    height: 80px;
    width: 80px;
    border-radius: 50%;
    margin: auto;
    margin-top: -40px;
  }
  h1 {
    text-align: center;
  }
</style>