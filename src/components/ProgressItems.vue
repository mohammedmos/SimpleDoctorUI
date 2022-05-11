<template>
<div v-for="n in numbers" :key="n" >
  <ProgressBar :width="n"/>
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