<template>
  <p>{{title}}</p>
</template>

<script>
export default {
  name: 'test',
  props: {
    title: {
      type: String,
      required: true
    }
  }
}
</script>