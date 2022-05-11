<template>
  <div class="px-4  mx-auto py-1">
    <div v-for="(doctor,index) in doctors" :key="index" class="grid  mx-5 md:grid-cols-2 sm:grid-cols-1 lg:max-w-screen-lg my-3 ">
      <router-link :to="'/new'"><ListItem :doctor="doctor"/>
        <hr>
      </router-link>

    </div>
  </div>

</template>

<script>
import ListItem from '@/components/ListItem.vue'

export default {
  name: "ListItems",
  props: ['doctors'],
 components: {
    ListItem
  },

}
</script>

<style scoped>

</style>