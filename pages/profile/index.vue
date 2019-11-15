<template>
  <div>
    <div class="profile__picture">
      <div class="profile__picture_cover"/>
      <img src="icon.png" alt="profile">
      <h1>Prenom Nom</h1>
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
      <button :class="[selectedItem === 'info' ? 'selectedButton' : '']">Mes infos</button>
      <button :class="[selectedItem === 'document' ? 'selectedButton' : '']">Documents</button>
      <button :class="[selectedItem === 'search' ? 'selectedButton' : '']">Ma recherche</button>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'profile',
  data(){
    return {
      selectedItem: 'info'
    }
  }
}
</script>

<style scoped>
  .profile__nav {
    width: 90%;
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
    width: 90%;
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
    background: rgba(125, 125, 125, .7);
  }
  .profile__complete_progression div:first-child {
    background: #000;
  }
  h1 {
    font-weight: 400;
    margin: 2vh 0;
    font-size: 1.5em;
  }
  img[alt=profile]{
    display: block;
    height: 70px;
    width: 70px;
    border-radius: 50%;
    border: 1px solid black;
    margin: auto;
    margin-top: -35px;
  }
  h1 {
    text-align: center;
  }
</style>