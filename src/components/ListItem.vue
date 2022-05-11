<template>

        <div class="grid  md:grid-cols-3 grid-cols-3 mb-4">
          <div class="relative w-24 h-24 max-h-full rounded-xl shadow sm:h-24">
            <img class="absolute object-cover w-24 h-24 rounded-xl" src="https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg?auto=compress&amp;cs=tinysrgb&amp;dpr=3&amp;h=750&amp;w=1260" alt="Person" />
          </div>
          <div class="flex flex-col justify-start col-span-2 md:col-md-1 py-3 ">
            <p class="text-xs font-bold text-left text-cyan-700">{{ doctor.name }}</p>
            <p class="text-xs text-left text-gray-500 font-bold"> Spécialité: {{ doctor.branch }}</p>
            <p class="text-xs text-left text-gray-500">
              {{ doctor.localization }}
            </p>
            <div class="flex justify-between content-center">
                <p class="text-gray-500 "><i class="fa fa-map-marker-alt fa-sm"></i> <span class="text-xs">Alger</span></p>
                <div>
                    <Rating/>
                </div>
            </div>
          </div>
        </div>



</template>
<script>
import Rating from "@/components/Rating";
export default {
  name: 'ListItem',
  props:['doctor'],
  components:{
    Rating
  }
}
</script>
