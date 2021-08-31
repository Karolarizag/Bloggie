<template>
  <div height="50">
    <v-app-bar flat app color="first">
      <v-btn text color="white">Bloggie</v-btn>
      <v-spacer></v-spacer>
      <v-btn icon color="third"><v-icon>mdi-magnify</v-icon></v-btn>
      <v-btn text color="third">Log in</v-btn>  
      <v-btn text color="third">Sign up</v-btn>  
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>