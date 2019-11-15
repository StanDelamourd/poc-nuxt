<template>
  <div>
    <div class="profile__picture">
      <div class="profile__picture_cover"/>
      <img src="icon.png" alt="profile">
      <h1>Prenom Nom</h1>
    </div>
    <div class="profile__complete">
      <p>Augmentez vos chances de trouver un emploi en completant votre profil</p>
      <div/>
      <div/>
      <div/>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'profile'
}
</script>

<style scoped>
  .profile__picture_cover {
    width: 100%;
    height: 10vh;
    background: grey;
  }
  .profile__complete{
    background: rgba(125, 125, 125, .5);
    width: 95%;
    margin: auto;
    padding: 10px;
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