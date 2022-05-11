<template>
  <div class="grid gap-2 md:grid-cols-4  grid-cols-4 mb-4">
    <div class="relative w-16 h-16 max-h-full rounded-xl shadow ">
      <img class="absolute object-cover w-16 h-16 rounded-xl" src="https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg?auto=compress&amp;cs=tinysrgb&amp;dpr=3&amp;h=750&amp;w=1260" alt="Person" />
    </div>
    <div class="flex flex-col justify-start col-span-2 md:col-md-1 py-3 ">
      <p class="text-xs font-semibold text-left text-cyan-700">{{ doctor.name }}</p>
      <p class="text-xs text-left text-gray-500 font-normal"> 1 month</p>

    </div>
    <div class="w-2/4 text-right py-1 " >
      <div class="flex justify-end rounded-lg border  border-yellow-200 ">
        <span class="text-yellow-500">5</span>
        <svg aria-hidden="true" focusable="false" data-prefix="fas" data-icon="star" class="w-4 text-yellow-500 mr-1" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
          <path fill="currentColor" d="M259.3 17.8L194 150.2 47.9 171.5c-26.2 3.8-36.7 36.1-17.7 54.6l105.7 103-25 145.5c-4.5 26.3 23.2 46 46.4 33.7L288 439.6l130.7 68.7c23.2 12.2 50.9-7.4 46.4-33.7l-25-145.5 105.7-103c19-18.5 8.5-50.8-17.7-54.6L382 150.2 316.7 17.8c-11.7-23.6-45.6-23.9-57.4 0z"></path>
        </svg>
      </div>
    </div>
  </div>
  <p class="text-xs text-left text-gray-500 font-normal "> Many thanks to doctor Dr. Amine Mohamed He is Professional and competent...</p>

</template>

<script>

export default {
  name: "ResponsiveItem",
  props:['doctor'],
  components:{

  }
}
</script>

<style scoped>

</style>