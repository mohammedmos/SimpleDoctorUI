<template>
  <div class=" relative grid justify-items-stretch  ">
    <div class="relative w-28 h-28 max-h-full rounded-xl justify-self-center shadow mt-n16 sm:h-24 "  >
      <img class="absolute object-cover w-28 h-28 rounded-xl"  src="https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg?auto=compress&amp;cs=tinysrgb&amp;dpr=3&amp;h=750&amp;w=1260" alt="Person" />
    </div>
    <div class="bg-gray-100 rounded-xl pt-20 " style="margin-top: -60px">
      <p class="text-md text-center font-semibold text-cyan-700">{{ doctor.name }}</p>
      <p class="text-md text-center text-gray-500 font-semibold"> Spécialité: {{ doctor.branch }}</p>
      <p class="text-md text-center text-gray-500 mt-6">
        {{ doctor.localization }}
      </p>
      <p class="text-gray-500 text-center "><i class="fa fa-map-marker-alt fa-sm"></i> <span class="text-md">Alger</span></p>
      <Review/>
    </div>


  </div>

</template>

<script>
import Review from "@/components/Review";

export default {
  name: "SlideComponent",
  components:{
    Review,
  },
  data(){
    return{
      message:"test",
      doctor: {
        name:"Dr. Amine Mohamed",
        branch:"Chirurgie dentaire",
        localization:"CHU Mustapha",
        wilaya:"Alger",
      },
      mobile: false,

    }
  },
}
</script>

<style scoped>

</style>