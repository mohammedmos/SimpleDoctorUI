<template>
<div v-for="(n,index) in numbers" :key="index" >
  <div class="grid grid-cols-10 content-center">
    <p class="text-cyan-700" style="margin-right:4px;">{{index+1}}</p>
    <div class="col-span-9">
      <ProgressBar :width="n"/>
    </div>


  </div>
</div>
</template>

<script>
import ProgressBar from "@/components/ProgressBar";
export default {
  name: "ProgressItems",
  components:{
    ProgressBar
  },
  data() {
    return {
      numbers: [80, 50, 60, 40, 20 ]

    };
  },
}
</script>

<style scoped>

</style>