<template>
  <div class="mt-15">
      <h1>NEWS</h1>
      <v-divider />
      <div
        v-for="(item, idx) in category"
        :key="idx"
        class="px-10 py-5">
        <v-row>

          <v-col cols="5">
            <v-img 
              max-height="300"
              max-width="500"
              :src="item.multimedia" />
          </v-col>

          <v-col>
            <v-row>
              <v-col cols="12">
                <h2>{{item.title.toUpperCase()}} </h2>
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="12">
                <p>{{item.subtitle}}</p>
              </v-col>
            </v-row>
            <v-row  class="d-flex align-end">
              <v-col cols="12">
                <p>{{item.creator.username}}</p>
              </v-col>
            </v-row>
          </v-col>

        </v-row>
      </div>
    </div>
</template>

<script>
export default({
  name: 'News', 
  props: {
    category: Array,
  },
})
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Fjalla+One&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Kaisei+HarunoUmi&display=swap');

h2 {
  font-family: 'Fjalla One', sans-serif;
  text-decoration: underline;
  font-size: 34px;
}
h1 {
  font-family: 'Fjalla One', sans-serif;
  text-decoration: underline;
  font-size: 50px;
}
p {
  font-family: 'Kaisei HarunoUmi', serif;
  font-size: 19px;
}
</style>