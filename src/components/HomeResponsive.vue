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
      <p class="font-bold text-black text-left mx-5 my-4 text-lg">A la une </p>
      <div class="grid grid-cols-4 md:grid-cols-4 sm:grid-cols-1 xs:grid-cols-1 gap-8 mx-16">
        <div v-for="element in message" :key="element">
          <router-link :to="'/new'">
          <Slide></Slide>
          </router-link>
        </div>

      </div>
      <p class="font-bold text-black text-left mx-5 my-4 text-lg">Recommended</p>

      <ListItemsResponsive :doctors="doctor"/>
    </div>
  </div>

</template>

<script>
import ListItemsResponsive from '@/components/ListItemsResponsive.vue';
import Filters from "@/components/Filters";
import Slide from '@/components/Slide'
export default {
  name: "HomeResponsive",
  components: {
    ListItemsResponsive,
    Filters,
    Slide
  },
  data(){
    return{
      message:[1,2,3,4],
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
          if(window.innerWidth <= 500) {
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