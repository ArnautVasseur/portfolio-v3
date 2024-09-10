<template>
  <div class="box">
    <div class="label">{{ label }}</div>
    <div class="content">
      <icon-school v-if="iconType === 'school'"/>
      <icon-pro v-else-if="iconType === 'pro'" />
      <icon-bulb v-else />
      <h2>{{ content }}</h2>
    </div>
  </div>
</template>

<script lang="ts" setup>


// @ts-ignore
const props = withDefaults(
  // @ts-ignore
  defineProps<{
    label: string;
    content: string;
  }>(), 
  {
    label: '',
    content: ''
  }
);

const iconType = computed(() => {
  if (props.label.includes("School")) {
    return "school";
  } else if (props.label.includes("Professional")) {
    return "pro";
  } else {
    return "other";
  }
});

</script>

<style scoped lang="scss">

.box {
  width: 230px;
  height: 130px;
  color: $background-100;
  font-family: $Sen;
  text-align: center;
  filter: drop-shadow(0px 0px 40px rgb(0, 0, 0, 20%));
}

.label {
  position: relative;
  width: 100%;
  height: 50%;
  padding: 10px;
  background: $primary-300;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.5rem;
  font-family: $Sen;
  clip-path: polygon(
    0 25%,
    10% 0,
    90% 0,
    100% 25%,
    100% 100%,
    0 100%
  );
}

.content {
  width: 100%;
  height: 50%;
  background-size: 100% 100%;
  background-position: 0px 0px;
  background-image: radial-gradient(50% 91% at 50% 50%, #FFFFFFFF 1%, #F4EED6 100%);
  color: $primary-300;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 30px;
  font-size: 2.5rem;
  font-weight: 700;
  font-family: $KyoMadoka;
  clip-path: polygon(
    0 0%,
    100% 0,
    100% 75%,
    90% 100%,
    10% 100%,
    0 75%
  );
}

</style>