<template>
  <v-card 
    width="400"
    outlined
    tile
    style="border: none"> 
    <v-img 
      max-height="250"
      min-height="250"
      max-width="400"
      min-width="400"
      :src="post.multimedia" />

    <h3>
      {{post.title}}
    </h3>
    <p>
      {{post.subtitle}}
    </p>
    <p>
      {{post.creator.username}}
    </p>
  </v-card>
</template>

<script>
export default ({
  name: 'PostCard',
  props: {
    post: Object
  },
})
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Fjalla+One&display=swap');

h3 {
  font-family: 'Fjalla One', sans-serif;
  font-size: 30px;
}
</style>