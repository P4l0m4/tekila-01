<template>
  <div id="app">
    <div class="gradient"></div>
    <HeaderComponent />
    <CirclesComponent />
    <DemoComponent />

    <FooterComponent />
  </div>
</template>
<script>
import HeaderComponent from "@/components/HeaderComponent.vue";
import FooterComponent from "@/components/FooterComponent.vue";
import CirclesComponent from "@/components/CirclesComponent.vue";
import DemoComponent from "@/components/DemoComponent.vue";

export default {
  components: {
    HeaderComponent,
    FooterComponent,
    CirclesComponent,
    DemoComponent,
  },
};
</script>

<style lang="scss" scoped>
#app {
  background-image: url("@/assets/header.jpg");
  background-size: cover;
  position: relative;
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
  gap: $big-gap;

  .gradient {
    position: absolute;
    width: 100vw;
    height: 100vh;
    top: 0;
    right: 0;
    z-index: 0;
    background: linear-gradient(
      180deg,
      rgba(49, 35, 153, 0) 0%,
      $base-color 100%
    );
  }
}
</style>
