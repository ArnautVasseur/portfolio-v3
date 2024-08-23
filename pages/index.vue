<script setup lang="ts">

</script>

<template>
  <div class="container">
    <div class="left">

    </div>

    <div class="right">
      <div class="background"></div>
      <button-header></button-header>
    </div>

  </div>
</template>

<style scoped lang="scss">

.container{
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;

  .left, .right{
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    // border: 1px solid blue;
  }

  .left{
    width: 45%;
  }

  .right{
    width: 55%;
    overflow: hidden;
    position: relative;

    .background{
      position: absolute;
      width: 100%;
      height: 100%;
      filter: blur(5px);
      background-image: url(/public/backgrounds/buizel.jpg) ;
      transform: skew(-6deg) translate(50px);
    }
  }
}

</style>