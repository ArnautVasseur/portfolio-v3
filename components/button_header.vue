<template>
  <div
    class="button"
      @mouseenter="hovering = true"
      @mouseleave="hovering = false"
    >

    <arrow-icon class="arrow_icon"/>
    <project-icon class="svg_icon" :currentColor="hovering ? hoverColor : defaultColor"/>
    <h2>Discover my Projects</h2>
  </div>
</template>

<script lang="ts" setup>

const defaultColor = '#F4EED6';
const hoverColor = '#3A3732';
const hovering = ref(false);
</script>

<style scoped lang="scss">
.button {
  width: 690px;
  height: 145px;
  border-radius: 60px;
  font-family: $sen;
  background: $primary-200;
  font-size: 2.5rem;
  color: $secondary-100;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  cursor: pointer;
  transition: 300ms;
  position: relative;
  
  &::before {
    content: '';
    width: 670px;
    height: 130px;
    border-radius: 55px;
    background: none;
    border: 3px solid $secondary-100;
    position: absolute;
  }
}


.button:hover {
  background: $secondary-100;
  color: $primary-200;
}

.button:hover::before {
  border: 3px solid $primary-200;
}

.arrow_icon {
  position: absolute;
  scale: 0.15;
  left: -350px;
  opacity: 0;
  transition: all 0.3s ease;
}

.button:hover .arrow_icon {
  left: -270px;
  opacity: 1;
}
</style>
