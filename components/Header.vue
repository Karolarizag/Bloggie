<template>
    <v-toolbar flat class="d-flex justify-center fixed-bar" color="black" >  
      <v-btn v-for="(item, idx) in items" :key="idx" :to="{path: `${item.path}`}" text color="white">{{item.name}}</v-btn>
    </v-toolbar>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      menu: false,
      items: [
        {
          name: "News",
          path: '/news'
        },
        {
          name: 'Politics', 
          path: '/politics'
        },
        {
          name: 'Entertaiment', 
          path: '/entertaiment'
        }, 
        {
          name: 'Life', 
          path: '/life'
        }, 
        {
          name: 'Personal', 
          path: '/personal'
        }, 
        {
          name: 'Shopping', 
          path: '/shopping'
        }, 
        {
          name: 'Video',
          path: '/video'
        }
      ]
    }
  },
}
</script>