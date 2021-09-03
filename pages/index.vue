<template>
  <v-container fluid class="pa-0">
    <v-card 
      v-for="(item, idx) in items"
      :key="idx"
      tile 
      outlined 
      class="mt-15 py-8 px-5">
      <v-card-title> {{item.name.toUpperCase()}} </v-card-title>
      <v-divider></v-divider>
      {{item}}
      <v-card 
        v-for="(post, id) in feed" 
        :key="id"
        tile 
        outlined >
        <v-card-title>{{post.title}}</v-card-title>
        <v-card-text>
          <v-row>
            <v-col>
              <v-img max-height="200" max-width="200" :src="post.multimedia" />
            </v-col>
            <v-col>
              {{post.content}}
            </v-col>
          </v-row>
        </v-card-text>
        <v-card-actions>
          <v-row>
            <v-col>
              {{post.creator}}
            </v-col>
            <v-col>
              <v-btn text>Go there!</v-btn>
            </v-col>
          </v-row>
        </v-card-actions>
        
      </v-card>
    </v-card>
  </v-container>  
</template>

<script>
export default({
  async asyncData ({ $axios, params }) {
    const news = await $axios.$post('/post/category', {category: 'News'})
    const politics = await $axios.$post('/post/category', {category: 'Politics'})
    const entertaiment = await $axios.$post('/post/category', {category: 'Entertaiment'})
    const life = await $axios.$post('/post/category', {category: 'Life'})
    const personal = await $axios.$post('/post/category', {category: 'Personal'})
    const shopping = await $axios.$post('/post/category', {category: 'Shopping'})
    const video = await $axios.$post('/post/category', {category: 'Video'})
    return { feed: [news, politics, entertaiment, life, personal, shopping, video]  }
  }, 
  data() {
    return {
      items: [
        {
          name: "News",
          path: '/news', 
          posts: this.news
        },
        {
          name: 'Politics', 
          path: '/politics',
          posts: this.politics
        },
        {
          name: 'Entertaiment', 
          path: '/entertaiment',
          posts: this.entertaiment
        }, 
        {
          name: 'Life', 
          path: '/life',
          posts: this.life
        }, 
        {
          name: 'Personal', 
          path: '/personal',
          posts: this.personal
        }, 
        {
          name: 'Shopping', 
          path: '/shopping',
          posts: this.shopping
        }, 
        {
          name: 'Video',
          path: '/video',
          posts: this.video
        }
      ]
    }
  },
})
</script>
