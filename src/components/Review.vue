<template>
<div class="py-4 mx-6">
  <div class="grid gap-4 grid-cols-2 text-gray-500">
    <div>
      <p class="text-md pl-6  text-gray-500 text-left">Rating</p>
      <p class="font-md text-6xl">4.3</p>
      <Rating/>
      <p class="text-xs pl-6 text-gray-500 text-left">40.000</p>

    </div>
    <div class="w-full">
      <ProgressItems/>
    </div>
  </div>
</div>
</template>

<script>
import Rating from "@/components/Rating";
import ProgressItems from "@/components/ProgressItems";
export default {
  name: "ReviewComponent",
  components:{
    Rating,
    ProgressItems
  }
}
</script>

<style scoped>

</style>