<template>
  <div>
    <Field :value="mail" label="Adresse mail" inputType="email"/>
    <Field :value="password" label="Mot de passe" inputType="password"/>
    <Field :value="confirmPassword" label="Confirmer le mot de passe" inputType="password"/>
  </div>
</template>

<script>
import Field from '../field';
export default {
  name: 'SecondStep',
  components: {
    Field
  },
  data(){
    return {
      mail: '',
      password: '',
      confirmPassword: ''
    };
  }
}
</script>
<style scoped>

</style>