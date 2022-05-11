<template>
  <div  class=" ">

    <div class="flex justify-between px-20 bg-cyan-700 py-4 shadow-lg">
      <div class="flex">
        <p class="font-bold text-left text-xl text-white flex flex-col">
            <span>
              DO
            </span>
          <span>
              CS
            </span>
        </p>
        <p class="font-bold text-white text-left mx-16 my-4 text-lg">Let's find you a doctor</p>
      </div>


      <div class="my-2">
        <div class="bg-gray-100 p-1 rounded-xl">
          <span class="material-symbols-outlined text-gray-400 ">person</span>
        </div>
      </div>
    </div>

    <Filters/>

    <div class="  w-full  md:px-6  py-2 ">
      <ListItemsResponsive :doctors="doctor"/>
    </div>
  </div>

</template>

<script>
import ListItemsResponsive from '@/components/ListItemsResponsive.vue';
import Filters from "@/components/Filters";
export default {
  name: "HomeResponsive",
  components: {
    ListItemsResponsive,
    Filters
  },
  data(){
    return{
      message:"test",
      doctor:[
        {
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },{
          name:"Dr. Amine Mohamed",
          branch:"Chirurgie dentaire",
          localization:"CHU Mustapha",
          wilaya:"Alger",
        },
      ],
      methods: {
        isMobile() {
          if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
            return true
          } else {
            return false
          }
        }
      }
    }
  }
}
</script>

<style scoped>

</style>