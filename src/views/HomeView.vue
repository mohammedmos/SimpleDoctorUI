<template>


  <div v-if="mobile" class="">

    <div class="flex justify-between mx-10 mt-8">
          <p class="font-bold text-left text-xl text-cyan-700 flex flex-col">
            <span>
              DO
            </span>
            <span>
              CS
            </span>
          </p>
        <div class="my-2">
          <div class="bg-gray-100 p-1 rounded-xl">
            <span class="material-symbols-outlined text-gray-400 ">person</span>
          </div>
        </div>
    </div>
    <div class="mt-4 mb-8 mx-5 ">
      <p class="font-bold text-black text-left mx-5 my-4 text-lg">Let's find you a doctor</p>
      <SearchBox />
      <p class="font-bold text-black text-left mx-5 my-4 text-lg">A la une </p>
      <Splide :options="{ rewind: true,preloadPages:3,wheel:true,gap:8 ,pagination:false,lazyLoad:true }" aria-label="My Favorite Images">
        <SplideSlide v-for="(index,doc) in doctor" :key="index">
          <Slide :doc="doc"/>
        </SplideSlide>

      </Splide>
      <p class="font-bold text-black text-left mx-5 my-4 text-lg">Recommended</p>

    </div>


    <div class=" sm:max-w-xl md:max-w-full lg:max-w-screen-xl md:px-24 lg:px-8 lg:py-20 bg-gray-100">
      <ListItems :doctors="doctor"/>
    </div>
  </div>
  <div v-else>
    <HomeResponsive/>

  </div>
</template>

<script>
// @ is an alias to /src
import ListItems from '@/components/ListItems.vue'
import SearchBox from "@/components/SearchBox";
import HomeResponsive from "@/components/HomeResponsive";
import { Splide, SplideSlide } from '@splidejs/vue-splide';
import '@splidejs/vue-splide/css';

// or other themes
import '@splidejs/vue-splide/css/skyblue';
import '@splidejs/vue-splide/css/sea-green';

// or only core styles
import '@splidejs/vue-splide/css/core';
import Slide from '@/components/Slide'
export default {
  name: 'HomeView',
  components: {
    ListItems,
    SearchBox,
    HomeResponsive,
    Splide,
    Slide,
    SplideSlide,
    },
  data(){
    return{
    mobile: false,
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
      },{
        name:"Dr. Amine Mohamed",
        branch:"Chirurgie dentaire",
        localization:"CHU Mustapha",
        wilaya:"Alger",
      },
    ],


    }
  },
  created() {
    if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
      this.mobile= true;
    } else {
      this.mobile= false;
    }
    window.addEventListener("resize", this.isMobile);


  },
  unmounted() {
    window.removeEventListener("resize", this.isMobile);
  }
  , methods: {
    isMobile() {
      if(window.innerWidth <= 1024) {
        this.mobile= true
      } else {
        this.mobile= false
      }
    }
  }
}
</script>
<style >
.splide__arrow svg{
  fill: gray !important;
}
</style>
