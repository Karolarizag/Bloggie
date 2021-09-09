<template>
  <div class="d-flex wrap mt-15 pa-n15">
    <PostCard 
      v-for="(item, id) in posts" 
      :key="id" 
      :post="item" 
      class="mr-7"/>
  </div>
</template>

<script>
export default ({
  async asyncData ({$axios}) {
    const posts = await $axios.$post('/post/category', {category: 'Life'})
    return { posts }
  }
})
</script>
