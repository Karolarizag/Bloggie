<template>
  <div v-if="category" class="mt-15">
      <NuxtLink :to="{path: `/${category[0].category.toLowerCase()}`}" style="color: black;">
        <h1>{{category[0].category.toUpperCase()}}</h1>
      </NuxtLink>
      <v-divider />
      <PostCard
        v-for="(item, idx) in category"
        :key="idx"
        :post="item"
        class="px-10 py-5" />
    </div>
</template>

<script>
export default({
  name: 'Category', 
  props: {
    category: Array
  },
})
</script>
