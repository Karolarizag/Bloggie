<template>
  <v-container fluid class="pa-0">
    <News :category="news" />
    <Category :category="politics" />
    <Category :category="entertaiment" />
    <Category :category="life" />
    <Category :category="personal" />
    <Category :category="shopping" />
    <!-- <Category :category="video" /> -->
  </v-container>  
</template>

<script>
export default({
  async asyncData ({ $axios, params }) {
    const posts = await $axios.$get('/post')
    const politics = await $axios.$post('/post/category', {category: 'Politics'})
    const entertaiment = await $axios.$post('/post/category', {category: 'Entertaiment'})
    const life = await $axios.$post('/post/category', {category: 'Life'})
    const personal = await $axios.$post('/post/category', {category: 'Personal'})
    const shopping = await $axios.$post('/post/category', {category: 'Shopping'})
    // const video = await $axios.$post('/post/category', {category: 'Video'})
    return { posts, politics, entertaiment, life, personal, shopping }
  }, 
  data() {
    return {
      newsS: 'NEWS'
    }
  },
  computed: {
    news() {
      const news = [...this.posts]
      return news
        .sort((a, b) => new Date(b.date) - new Date(a.date))
        .splice(0, 4)
    },
  },
})
</script>
