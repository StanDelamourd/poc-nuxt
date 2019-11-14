<template>
  <div>
    <p>{{title}}</p>
    <p>{{description}}</p>
  </div>
</template>

<script>
export default {
  name:"card",
  props:{
    title:{
      required:true,
      type:String,
    },
    description:{
      required:true,
      type:String,
    }

  }
}
</script>