<template>
  <div class="my-5">

    <div class="flex justify-between content-center  mx-10 my-16">
      <div class="my-2">
        <router-link :to="'/new'">
          <span class="material-symbols-outlined text-gray-300 mt-2">arrow_back</span>
        </router-link>
      </div>
      <div class="my-2">
        <div class="bg-gray-100 p-1 rounded-xl">
          <span class="material-symbols-outlined text-gray-400 ">person</span>
        </div>
      </div>
    </div>

    <div class="bg-gray-100 px-6 py-2">
      <ListItem :doctor="doctor"/>

    </div>
    <div class="px-10 mt-16 flex items-center justify-between">
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

    <div class="bg-gray-100 rounded-xl relative grid justify-items-stretch pb-10 mt-4 mx-10">
        <Calendar/>
    </div>
    <div class="mx-10">
      <button class=" bg-cyan-700 my-6 text-white active:bg-cyan-600 font-meduim uppercase w-full  px-4 py-2 rounded-lg  shadow hover:shadow-md outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button"
      >
        Confirmer
      </button>
    </div>

  </div>

</template>

<script>
import ListItem from "@/components/ListItem";
import Calendar from "@/components/Calendar";
export default {
  name: "ScheduleComponent",
  components:{
    ListItem,
    Calendar
  },
  data(){
    return{
      message:"test",
      doctor: {
        name:"Dr. Amine Mohamed",
        branch:"Chirurgie dentaire",
        localization:"CHU Mustapha",
        wilaya:"Alger",
      }
    }
  }
}
</script>

<style scoped>

</style>