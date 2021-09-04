<template>
  <v-container app fluid class="pa-0">
    <v-app-bar fixed flat color="black" >
      <v-row>
        <v-col cols="1">
          <v-btn icon color="white" @click="menu = !menu"><v-icon>mdi-menu</v-icon></v-btn>
        </v-col>
        <v-col cols="2">
          <NuxtLink :to="{path: '/'} ">
            <v-img 
              max-height="100"
              max-width="150" 
              class="mt-3 ml-n15"
              src="https://cdn.discordapp.com/attachments/754119455151358103/882602475910225950/BLOGGIE-logo.png">
            </v-img>
          </NuxtLink>
        </v-col>
        <v-col cols="6" class="d-flex justify-center">
          <v-btn v-for="(item, idx) in items" :key="idx" :to="{path: `${item.path}`}" text color="white">{{item.name}}</v-btn>
        </v-col>
        <v-col cols="3" class="d-flex justify-end">
          <v-btn text color="white">Log in</v-btn>
          <v-btn text color="white">Join</v-btn>
        </v-col>
      </v-row>
    </v-app-bar>

    <v-navigation-drawer
        v-model="menu"
        app
        temporary
        dark
        width="400"
        color="grey darken-4">
        <v-list-item>
          <v-btn class="mt-10 ml-3" icon dark @click="menu = false"><v-icon>mdi-close</v-icon></v-btn>
        </v-list-item>
        <div class="px-5 py-10">
          <v-divider dark />
        </div>
        <v-list-item 
          v-for="(item, idx) in items" 
          :key="idx"
          class="mt-3">
          <v-btn text dark :to="{path: `${item.path}`}">{{item.name}}</v-btn>
        </v-list-item>
        <div class="px-5 py-10">
          <v-divider dark />
        </div>
        <v-row class="px-8">
          <v-col xl="5" lg="5" md="5" sm="5" xs="12">
            <p style="color: white;" class="mt-2">Follow us</p>
          </v-col>
          <v-col>
            <v-btn icon dark><v-icon>mdi-facebook</v-icon></v-btn>
          </v-col>
          <v-col>
            <v-btn icon dark><v-icon>mdi-twitter</v-icon></v-btn>
          </v-col>
          <v-col>
            <v-btn icon dark><v-icon>mdi-instagram</v-icon></v-btn>
          </v-col>
        </v-row>
        <div class="px-5 py-10">
          <v-divider dark />
        </div>
        <v-row>
          <v-col class="d-flex justify-center">
            <p style="color: white;" >This is a practice project, inpired in HuffPost!</p>
          </v-col>
        </v-row>
        <v-row class="mt-n8">
          <v-col class="d-flex justify-center">
            <v-btn text dark >
              <a style="text-decoration: none; color: white;" href="https://www.huffpost.com/" target="blank">Go there!</a>
            </v-btn>
          </v-col>
        </v-row>

    </v-navigation-drawer>
  </v-container>
</template>

<script>
export default {
  name: 'Headerscroll',
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
        // {
        //   name: 'Video',
        //   path: '/video'
        // }
      ]
    }
  },
}
</script>


<style scoped>
  .fixed-bar {
    position: sticky;
    top: 0.1px;
    z-index: 8;
  }
</style>