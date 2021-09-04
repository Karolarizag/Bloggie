<template>
  <div class="mt-15">
      <h1>{{category[0].category.toUpperCase()}}</h1>
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
  name: 'Category', 
  props: {
    category: Array,
  },
})
</script>
