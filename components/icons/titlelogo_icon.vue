<template>
  <svg :width=Width :height=Height viewBox="0 0 384 384" fill="none" xmlns="http://www.w3.org/2000/svg">
    <circle cx="192" cy="192" r="187" stroke="#F4EED6" stroke-width="10"/>
    <circle cx="192.5" cy="192.5" r="159.5" fill="#F4EED6"/>
    <rect x="58" y="191.953" width="189.439" height="189.439" rx="15" transform="rotate(-45 58 191.953)" fill="#233A57"/>
    <circle cx="192.5" cy="192.5" r="58.5" stroke="#F4EED6" stroke-width="10"/>
    <circle cx="192" cy="192" r="28" fill="#F4EED6"/>
  </svg>
</template>

<script lang="ts" setup>

// @ts-ignore
const props = defineProps({
  Width:String,
  Height:String
})
</script>

<style>

</style>