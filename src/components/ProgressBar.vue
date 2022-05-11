<template>

  <div class="relative pt-2">
    <div class="overflow-hidden h-2 mb-4 text-xs flex rounded bg-gray-200">
      <div :style="style"  class="shadow-none flex flex-col text-center whitespace-nowrap text-white justify-center bg-cyan-700"></div>
  </div>
  </div>
</template>

<script>
export default {
  name: "ProgressBar",
  props:['width'],
  computed: {
    style () {
      return 'width: ' +  this.width+'%';
    }
  },
}
</script>

<style scoped>

</style>