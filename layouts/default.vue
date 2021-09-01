<template>
  <v-app>
  <v-main>
    <Bloggie />
    <Header v-on:scroll="isScrolling = !isScrolling" v-if="!isScrolling" />
    <Header-scroll v-if="isScrolling" />
    <v-container>
      <Nuxt />
    </v-container>
  </v-main>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      isScrolling: false, 
    }
  },
}
</script>