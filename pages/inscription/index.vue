<template>
<div>
  <Test v-for="item in items" :key="item.title" :title="item.title"/>
  <p v-if="isDisplay">{{title}}</p>
  <p v-else>ookok</p>
</div>  

</template>

<script>
import Test from '../../components/test/index';
export default {
data () {
    return {
      isDisplay: false,
      title: 'Vuetify.js',
      items: [
        {
          title: 'first'
        },
        {
          title: 'first'
        }
      ]
    }
  },
  components:{
    Test
  }
}
</script>