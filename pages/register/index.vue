<template>
  <div>
    <div class="form">
      <form>
        <FirstStep v-if="step === 1"/>
        <SecondStep v-else-if="step === 2"/>
        <ThirdStep v-else-if="step === 3"/>
        <FourthStep v-else-if="step === 4"/>
        <FivethStep v-else-if="step === 5"/>
        <SixthStep v-else-if="step === 6"/>
      </form>
    </div>
    <Button title="Suivant" :clickEvent="changeStep"/>
  </div>  
</template>
<script>
import FirstStep from '../../components/firstStep';
import SecondStep from '../../components/secondStep';
import ThirdStep from '../../components/thirdStep';
import FourthStep from '../../components/fourthStep';
import FivethStep from '../../components/fivethStep';
import SixthStep from '../../components/sixthStep';

import Button from '../../components/button';

export default {
  data () {
    return {
      step: 1,
    }
  },
  components:{
    FirstStep,
    SecondStep,
    ThirdStep,
    FourthStep,
    FivethStep,
    SixthStep,
    Button,
  },
  methods:{
    changeStep(){
      this.step += 1;
    }
  }
}
</script>

<style scoped>
  div >>> .fullButton {
    position: absolute;
    left: 50%;
    bottom: 5vh;
    transform: translate(-50%, 0);
    width: 95%;
  }
  .form {
    height: 90vh;
    display: flex;
    align-items: center;
  }
  form {
    width: 100%;
  }
</style>