<template>
  <v-container fluid class="pa-0">
    <div class="d-flex flex-wrap flex-row justify-center mx-5">
      <PostCard 
        v-for="(item, id) in posts" 
        :key="id" 
        :post="item" 
        class="mr-7"/>
    </div>
  </v-container>
</template>

<script>
export default ({
  async asyncData ({$axios}) {
    const posts = await $axios.$get('/post')
    posts
      .sort((a, b) => new Date(b.date) - new Date(a.date))
      .splice(0, 15)

    return {posts}
  }
})
</script>
