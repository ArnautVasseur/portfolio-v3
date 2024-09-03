<template>
  <svg :width=Width :height=Height viewBox="0 0 384 322" fill="none" xmlns="http://www.w3.org/2000/svg">
    <path d="M120.501 0.5C69.0004 63.5 -7.49963 175.5 120.501 322C-67.5 234.5 -7.49987 43 120.501 0.5Z" fill="white"/>
    <path d="M264 0C315.5 62.902 392 174.728 264 321C452.001 233.636 392.001 42.4339 264 0Z" fill="white"/>
    <circle cx="192" cy="161" r="71" stroke="white" stroke-width="40"/>
    <path d="M113.5 115.5C70.7 66.3 41 18.3333 31.5 0.5C76.7 24.1 126.667 65 146 82.5L113.5 115.5Z" fill="white"/>
    <path d="M147 239.5C97.8 282.3 49.8333 312 32 321.5C55.6 276.3 96.5 226.333 114 207L147 239.5Z" fill="white"/>
    <path d="M270.5 207C313.3 256.2 343 304.167 352.5 322C307.3 298.4 257.333 257.5 238 240L270.5 207Z" fill="white"/>
    <path d="M237 83C286.2 40.2 334.167 10.5 352 1C328.4 46.2 287.5 96.1667 270 115.5L237 83Z" fill="white"/>
  </svg>
</template>

<script lang="ts" setup>

// @ts-ignore
const props = defineProps({
  Width:String,
  Height:String
})

</script>

<style scoped lang="scss">



</style>