<template>
<div class="grid grid-cols-7">
  <div class="col-span-2 shadow-lg">
    <p class="font-smibold text-md text-black text-center py-6 mt-6 ">Similar</p>
    <div class="my-5 bg-gray-100 px-6 py-8">
      <div v-for="(doc,index) in doctors" :key="index">
        <router-link to="/new">
          <ListItem :doctor="doc"/>
        </router-link>

        <hr class="mb-2">
      </div>
    </div>
  </div>
  <div class="col-span-5 ">
    <div class="flex justify-between px-20 bg-cyan-700 pt-8 pb-24 shadow-lg">
      <div class="my-2">
        <router-link :to="'/'">
          <span class="material-symbols-outlined text-white mt-2">arrow_back</span>
        </router-link>
      </div>


      <div class="my-2">
        <div class="bg-gray-100 p-1 rounded-xl">
          <span class="material-symbols-outlined text-gray-400 ">person</span>
        </div>
      </div>
    </div>
    <div class="grid grid-cols-3">
      <div class="col-span-2 ">
        <div class="grid  md:grid-cols-3 grid-cols-3 mx-20 mb-4">
          <div class="relative w-40 h-40 max-h-full rounded-xl shadow sm:h-24" style="margin-top: -60px;">
            <img class="absolute object-cover w-40 h-40 rounded-xl" src="https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg?auto=compress&amp;cs=tinysrgb&amp;dpr=3&amp;h=750&amp;w=1260" alt="Person" />
          </div>
          <div class="flex flex-col justify-start col-span-2 md:col-md-1 py-3 ml-8">
            <p class="font-medium text-2xl text-left text-cyan-700">{{ doctor.name }}</p>
            <p class="text-normal text-left text-gray-500 font-medium "> Spécialité: {{ doctor.branch }}</p>

            <div class="flex  content-center">
              <p class="text-sm text-left text-gray-400 mt-2">
                {{ doctor.localization }}
              </p>
              <p class="text-gray-500 mx-6 content-center py-1"><i class="fa fa-map-marker-alt fa-sm "></i> <span class="text-sm mt-n1">Alger</span></p>

            </div>
          </div>
        </div>
        <div class="bg-gray-100 my-4 rounded-lg mx-20 py-4">
          <p class="mx-auto text-gray-500 text-4xl my-4 font-light mb-8">Rating</p>
          <div class="grid  grid-cols-2 text-gray-500">
            <div>
              <p class="font-md text-8xl">4.3</p>
              <RatingResponsive/>
              <p class="text-xs ml-16 text-gray-500 text-left">40.000</p>

            </div>
            <div class="w-5/6">
              <ProgressItems/>
            </div>
          </div>
        </div>

      </div>
      <div class="px-6">
        <button type="button"  v-on:click="toggleModal()" class="bg-cyan-700 my-6 text-white active:bg-cyan-600 font-meduim uppercase w-full  px-4 py-2 rounded-lg  shadow hover:shadow-md outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150"
        >
          Prendre rendez-vous
        </button>
        <div>
          <div v-for="(doc,index) in doctors" :key="index">
            <div class="bg-gray-100 rounded-lg p-2 my-4">
              <router-link to="/new">
              <ResponsiveItem :doctor="doc"/>
              </router-link>

            </div>
          </div>
        </div>
      </div>

    </div>

  </div>
</div>
  <div v-if="showModal" class="overflow-scroll fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex">
    <div class="relative w-auto my-6 mx-auto ">
      <!--content-->
      <div class="  border-0 rounded-lg shadow-lg rounded-lg relative flex flex-col w-full bg-white outline-none focus:outline-none">
        <!--header-->
        <button type="button" class="text-right" v-on:click="toggleModal()" style="margin-top: -12px">
          <i class="fas fa-times-circle text-black fa-2x"  ></i>

        </button>
        <div class="flex items-start justify-center px-6 pt-0 pb-6 rounded-t" >
<!--          <i class="fa fa-close text-white bg-black px-2 rounded-lg"></i>-->
          <h3 class="text-xl text-center  font-semibold text-black">
            Take an appointment with
          </h3>
<!--          <button class="p-1 ml-auto bg-transparent border-0 text-black opacity-5 float-right text-3xl leading-none font-semibold outline-none focus:outline-none" v-on:click="toggleModal()">-->
<!--              <span class="bg-transparent text-black opacity-5 h-6 w-6 text-2xl block outline-none focus:outline-none">-->
<!--                ×-->
<!--              </span>-->
<!--          </button>-->
        </div>
        <div class="my-5 bg-gray-100  px-4 rounded-xl  mx-4 pt-4">
            <ListItem :doctor="doctor"/>
        </div>
        <!--body-->
        <div class="px-10  flex items-center justify-between">
          <span  tabindex="0" class="focus:outline-none  text-base font-bold dark:text-gray-100 text-gray-800">Septembre</span>
          <div class="flex items-center">
            <button aria-label="calendar backward" class="focus:text-cyan-400 hover:text-cyan-400 text-cyan-700 dark:text-gray-100">
              <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-chevron-left" width="24" height="24" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                <path stroke="none" d="M0 0h24v24H0z" fill="none" />
                <polyline points="15 6 9 12 15 18" />
              </svg>
            </button>
            <button aria-label="calendar forward" class="focus:text-cyan-400 hover:text-cyan-400 ml-3 text-cyan-700 dark:text-gray-100">
              <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler  icon-tabler-chevron-right" width="24" height="24" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                <path stroke="none" d="M0 0h24v24H0z" fill="none" />
                <polyline points="9 6 15 12 9 18" />
              </svg>
            </button>

          </div>
        </div>

        <div class="bg-gray-100 rounded-xl relative grid justify-items-stretch mx-4 mt-4 ">
          <Calendar/>
        </div>
        <div class="mx-4 mb-4">
          <button class=" bg-cyan-700 my-4 text-white active:bg-cyan-600 font-meduim uppercase w-full  px-4 py-2 rounded-lg  shadow hover:shadow-md outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150"  type="button" v-on:click="toggleModal()">
            Confirmer
          </button>
        </div>
        <!--footer-->
<!--        <div class="flex items-center justify-end p-6 border-t border-solid border-slate-200 rounded-b">-->
<!--          <button class="text-red-500 bg-transparent border border-solid border-red-500 hover:bg-red-500 hover:text-white active:bg-red-600 font-bold uppercase text-sm px-6 py-3 rounded outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button" v-on:click="toggleModal()">-->
<!--            Close-->
<!--          </button>-->
<!--          <button class="text-red-500 background-transparent font-bold uppercase px-6 py-2 text-sm outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button" v-on:click="toggleModal()">-->
<!--            Save Changes-->
<!--          </button>-->
<!--        </div>-->
      </div>
    </div>
  </div>  <div v-if="showModal" class="opacity-25 fixed inset-0 z-40 bg-cyan-700"></div>
</template>

<script>
import ListItem from "@/components/ListItem";
import ProgressItems from "@/components/ProgressItems";
import RatingResponsive from "@/components/RatingResponsive";
import ResponsiveItem from "@/components/ResponsiveItem";
import Calendar from "@/components/Calendar";
export default {
  name: "AppointmentResponsive",
  components:{
    ListItem,
    ProgressItems,
    RatingResponsive,ResponsiveItem,Calendar
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
      doctors:[
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

      mobile: false,
      showModal: false

    }
  },
  methods: {
    toggleModal: function(){
      this.showModal = !this.showModal;
    }
  }
}
</script>

<style scoped>

</style>