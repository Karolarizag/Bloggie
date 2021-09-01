<template>
  <div>
    <v-toolbar 
      flat color="black" 
      height="250" 
      hide-on-scroll>
      <v-row class="mt-16">
        <v-col class="d-flex justify-start" cols="1">
          <v-btn icon color="white">
            <v-icon>mdi-menu</v-icon>
          </v-btn>
        </v-col>
        <v-col cols="9" class="d-flex justify-center">
          <v-img 
            max-height="100"
            max-width="330" 
            class="ml-15 mr-n15"
            src="https://cdn.discordapp.com/attachments/754119455151358103/882602475910225950/BLOGGIE-logo.png">
          </v-img>
        </v-col>
        <v-col cols="2" class="d-flex justify-end">
          <v-btn text color="white">Log in</v-btn>
          <v-btn text color="white">Join</v-btn>
        </v-col>
      </v-row>
    </v-toolbar>
  </div>
</template>

<script>
export default ({
  name: 'Bloggie',
})
</script>
