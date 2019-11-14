<template>
<div>
  <Card v-for="post in posts" :key="post.title" :title="post.title" :description="post.description"/>
  <Test v-for="item in items" :key="item.title" :title="item.title"/>
  <p v-if="isDisplay">{{title}}</p>
  <p v-else>ookok</p>
</div>  

</template>
<script>
import Test from '../../components/test/index';
import Card from '../../components/card/index';
export default {
  data () {
    return {
      user: {
        username: "jou",
        age: 12,
        
      },
      posts: [
        {
          title: 'First',
          description: 'second',
        },
        {
          title:'bis',
          description:'third',
        },
      ],
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
    Test,
    Card,
  }
}
</script>