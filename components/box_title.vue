import { ArceusL
  components: { titlelogo_icon },ogo } from '../.nuxt/components';
<template>
  <div class="container">
    <div class="top">
      <h2>Projet</h2>
    </div>

    <div class="separator">
      <hr class="hr-1">
      <titlelogo_icon class="icon" Height="50px"/>
      <hr class="hr-2">
    </div>
    
    <div class="bottom">
      <h3>{{ projectname }}</h3>
    </div>

    <arceus-logo class="icon_arc" Height="230px"/>
  </div>
</template>

<script lang="ts" setup>

// @ts-ignore
const props = defineProps({
  projectname:String
})

</script>

<style lang="scss" scoped>

.container {
  position: relative;
  overflow: hidden;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: white;

  .top,
  .bottom {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    box-shadow: inset 300px 0px 150px -50px $secondary-100, inset -300px 0px 150px -50px $secondary-100;
  }

  .top {
    margin-bottom: -2.5px;
    background: #354F60;
    height: 110px;
    font-size: 3.5rem;
    font-family: $KyoMadoka;
  }

  .bottom {
    margin-top: -2.5px;
    background: black;
    opacity: 0.9;
    height: 140px;
    font-size: 4rem;
    font-family: $Sen;
  }

  .separator {
    display: flex;
    width: 100%;
    position: relative;

    hr {
      width: 100%;
      height: 5px;
      background: $secondary-100;
      border: none;
      margin: 0;
      padding: 0;
      z-index: 2;

      &.hr-1 {
        clip-path: polygon(0 50%, 100% 0, 100% 100%);
      }

      &.hr-2 {
        clip-path: polygon(100% 50%, 0 0, 0 100%);
      }
    }
  }

  .icon, .icon_arc {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  .icon {
    z-index: 5;
  }

  .icon_arc {
    opacity: 0.1;
  }
}

</style>