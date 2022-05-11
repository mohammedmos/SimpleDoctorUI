<template>
  <div class=" mx-16 py-1 grid gap-4 grid-cols-3   my-3"  >
    <div v-for="(doctor,index) in doctors" :key="index" class="bg-gray-100 rounded-xl " >
      <div class=" mt-2 mx-3">
        <router-link :to="'/new'" >
          <ListItem :doctor="doctor"/>
        </router-link>
      </div>


    </div>
  </div>
</template>

<script>
import ListItem from '@/components/ListItem.vue'

export default {
  name: "ListItemResponsive",
  props: ['doctors'],
  components: {
    ListItem
  },
}
</script>

<style scoped>

</style>