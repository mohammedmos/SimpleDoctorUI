<template>
 <div class="justify-center mx-48" style="margin-top: -13px;">
   <div class="grid gap-4 grid-cols-3 justify-around w-full">
     <div class="col-span-2 mx-6">
       <div class=" relative flex w-full mx-auto text-gray-600 flex-wrap items-stretch mb-3  ">

         <svg class="text-gray-600 absolute  transform -translate-y-1/2 right-6 mt-5 mr-4 w-5 fill-current" xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" id="Capa_1" x="0px" y="0px"
              viewBox="0 0 56.966 56.966" style="enable-background:new 0 0 56.966 56.966;" xml:space="preserve"
              width="512px" height="512px">
            <path
                d="M55.146,51.887L41.588,37.786c3.486-4.144,5.396-9.358,5.396-14.786c0-12.682-10.318-23-23-23s-23,10.318-23,23  s10.318,23,23,23c4.761,0,9.298-1.436,13.177-4.162l13.661,14.208c0.571,0.593,1.339,0.92,2.162,0.92  c0.779,0,1.518-0.297,2.079-0.837C56.255,54.982,56.293,53.08,55.146,51.887z M23.984,6c9.374,0,17,7.626,17,17s-7.626,17-17,17  s-17-7.626-17-17S14.61,6,23.984,6z" />
          </svg>
         <input class="border-none bg-gray-100 shadow-lg w-full text-bold  h-10  px-5 pr-16 rounded-xl  focus:outline-none"
                type="search" name="search" placeholder="Search">

       </div>

     </div>


     <div class="relative flex   text-gray-600 flex-wrap items-stretch mb-3">
       <input class="border-none bg-gray-100 shadow-lg w-full text-bold  h-10  px-5 pr-16 rounded-xl  focus:outline-none"
              type="search" name="search" placeholder="Location">
       <span class="z-10 h-full leading-snug border-none font-normal absolute  text-gray-600 text-center absolute bg-transparent rounded text-base items-center justify-center w-8 right-0 pr-2 py-1">
<i class="fas fa-caret-down"></i>  </span>
     </div>
   </div>

 </div>
  <div class="py-2 px-20 flex justify-end">
    <div>
      <div class="bg-gray-100 p-1 rounded-xl">
        <span class="material-symbols-outlined text-gray-400 ">filter_alt</span>
      </div>
    </div>


  </div>
</template>

<script>

export default {
  name: "FiltersComponent",
  components:{
 }
}
</script>

<style scoped>

</style>