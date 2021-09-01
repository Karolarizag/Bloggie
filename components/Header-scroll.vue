<template>
  <div>
    <v-toolbar flat app color="black">
      <v-row>
        <v-col cols="1">
          <v-btn icon color="white"><v-icon>mdi-menu</v-icon></v-btn>
        </v-col>
        <v-col cols="2">
          <v-img 
            max-height="100"
            max-width="150" 
            class="mt-3 ml-n15"
            src="https://cdn.discordapp.com/attachments/754119455151358103/882602475910225950/BLOGGIE-logo.png">
          </v-img>
        </v-col>
        <v-col cols="6" class="d-flex justify-center">
          <v-btn text color="white">News</v-btn>
          <v-btn text color="white">Politics</v-btn>
          <v-btn text color="white">Entertaiment</v-btn>
          <v-btn text color="white">Life</v-btn>
          <v-btn text color="white">Personal</v-btn>
          <v-btn text color="white">Shopping</v-btn>
          <v-btn text color="white">Video</v-btn>
        </v-col>
        <v-col cols="3"></v-col>
      </v-row>
    </v-toolbar>
  </div>
</template>

<script>
export default {
  name: 'Header-scroll',
}
</script>