<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="95" height="95" viewBox="0 0 24 24"><path :fill=currentColor d="M11.112 12a4.502 4.502 0 0 0 8.777 0H22v8a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1v-8zM5 16h2v2H5zm10.5-2.5a2.5 2.5 0 1 1 0-5a2.5 2.5 0 0 1 0 5M11.111 10H2V4a1 1 0 0 1 1-1h18a1 1 0 0 1 1 1v6h-2.111a4.502 4.502 0 0 0-8.777 0"></path></svg>
</template>

<script lang="ts" setup>

// @ts-ignore
const props = defineProps({
  currentColor: String,
})
</script>