<template>
<div>
  <noSsr>
    <flickity ref="flickity" :options="flickityOptions" class="otherTest">
      <div class="carousel-cell">
        <div class="img__team">
          <img src="first.png" alt="team">
        </div>
        <h3>Inscrivez-vous <br/> sur A2JOB</h3>
      </div>
      <div class="carousel-cell">
        <div class="img__team">
          <img src="second.png" alt="trees" class="treesPicture"/>
        </div>
        <h3>Chercher un job</h3>
      </div>
      <div class="carousel-cell">
        <div class="img__team">
          <img src="last.png" alt="life" class="lifePicture"/>
        </div>
        <h3>Trouver un employe</h3>
      </div>
    </flickity>
  </noSsr>
  <button v-if="currentIndex === 2" @click="change">Suivant</button>
</div>
</template>

<script>
import Button from '../components/button';
import Flickity from 'vue-flickity';

export default {
  components: {
    Button,
    Flickity
  },
  data(){
    return {
      currentIndex: 0,
      flickityOptions: {
				initialIndex: 0,
				pageDots: true,
				wrapAround: false,
				prevNextButtons: false,
				freeScroll: false
			}
    }
  },
  mounted(){
		setTimeout(() => {
			this.$refs.flickity.on('change', (event) => {
				this.currentIndex = event;
			});
		}, 1000);
	},
  methods:{
    change() {
        this.$router.push({name: 'first'})
    }
  }
}
</script>
<style scoped>
  button {
    position: fixed;
    left: 5%;
    top: 80vh;
    display: block;
    color: white;
    width: 90%;
    margin: auto;
    padding: 20px 0;
    background: #FD5C63;
    border-radius: 20px;
  }
  h3{
    text-align: center;
    font-size: 2em;
    margin-top: 10vh;
  }
  .otherTest{
    height: 90vh;    
  }
  img {
    width: 80%;
    margin: 20vh auto 0 auto;
    display: block;
  }
  .home__button{
    margin-top: 25vh;
  }

  div >>> .flickity-page-dots .dot.is-selected {
    background: #FD5C63 !important;
  }
  div >>> .dot.is-selected {
    background: #FD5C63 !important;
  }
  .flickity-enabled {
    width: 100%;
	}
  .carousel-cell {
    width: 100%;
    height: 70vh;
	}
  .flickity-slider {
    transform: translateX(0)!important;
  }
</style>