<template>
  <div class="container">
    <div class="border"></div>
    <h1>Projects</h1>
  </div>
</template>

<script lang="ts" setup>

</script>

<style scoped lang="scss">

.container{
  position: relative;
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 550px;
  height: 130px;
  background-size: 100% 100%;
  background-position: 0px 0px;
  background-image: radial-gradient(50% 91% at 50% 50%, #FFFFFFFF 1%, #F4EED6 100%);
  font-size: 4rem;
  font-family: $KyoMadoka;
  color: $primary-100;
  font-weight: 700;
  border-radius: 15%;
  filter: drop-shadow(0px 0px 40px rgb(0, 0, 0, 20%));
}

.border{
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  margin: auto;
  width: 97%;
  height: 90%;
  border: 2px solid $primary-300;
  border-radius: 15%;
}

</style>