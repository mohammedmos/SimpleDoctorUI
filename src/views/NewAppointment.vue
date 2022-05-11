<template>
  <div v-if="mobile" class="my-5 mx-10">

    <div class="flex justify-between content-center  my-16">
      <div class="my-2">
        <router-link :to="'/'">
      <span class="material-symbols-outlined text-gray-300 mt-2">arrow_back</span>
        </router-link>
      </div>
      <div class="my-2">
        <div class="bg-gray-100 p-1 rounded-xl">
          <span class="material-symbols-outlined text-gray-400 ">person</span>
        </div>
      </div>
    </div>

    <div class="bg-gray-100 rounded-xl relative grid justify-items-stretch pb-10 ">
      <div class="relative w-32 h-32 max-h-full rounded-xl justify-self-center shadow mt-n16 sm:h-24 " style="top: -45px;">
        <img class="absolute object-cover w-32 h-32 rounded-xl"  src="https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg?auto=compress&amp;cs=tinysrgb&amp;dpr=3&amp;h=750&amp;w=1260" alt="Person" />
      </div>
      <p class="text-md text-center font-semibold text-cyan-700">{{ doctor.name }}</p>
      <p class="text-md text-center text-gray-500 font-semibold"> Spécialité: {{ doctor.branch }}</p>
      <p class="text-md text-center text-gray-500 mt-6">
        {{ doctor.localization }}
      </p>
      <p class="text-gray-500 text-center "><i class="fa fa-map-marker-alt fa-sm"></i> <span class="text-md">Alger</span></p>
        <Review/>

    </div>
    <router-link to="/schedule" class="bg-cyan-700 my-6 text-white active:bg-cyan-600 font-meduim uppercase w-full  px-4 py-2 rounded-lg  shadow hover:shadow-md outline-none focus:outline-none mr-1 mb-1 ease-linear transition-all duration-150" type="button"
    >
      Prendre rendez-vous
    </router-link>
  </div>
  <div v-else>
    <AppointmentResponsive />
  </div>
</template>

<script>
import Review from "@/components/Review";
import AppointmentResponsive from "@/components/AppointmentResponsive";
export default {
  name: "NewAppointment",
  components:{
    Review,
    AppointmentResponsive
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
  created() {
    if(window.innerWidth <= 1024) {
      this.mobile= true
    } else {
      this.mobile= false
    }
    window.addEventListener('resize', this.isMobile);

  }
  ,
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

<style scoped>

</style>