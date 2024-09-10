<template>
  <div class="paper" :style="{ transform: `rotate(${rotation}deg)` }"></div>
</template>

<script lang="ts" setup>

// @ts-ignore
const props = defineProps({
  rotation:Number
})

</script>

<style scoped lang="scss">

.paper{
  background: $background-100;
  width: 330px;
  height: 150px;
  box-shadow: 0 0 30px rgb(0, 0, 0, 40%);
  border-radius: 10px;
}

</style>