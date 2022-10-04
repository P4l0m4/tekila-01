<template>
  <div id="app">
    <HeaderComponent />
    <FooterComponent />
  </div>
</template>
<script>
import HeaderComponent from "@/components/HeaderComponent.vue";
import FooterComponent from "@/components/FooterComponent.vue";

export default {
  components: {
    HeaderComponent,
    FooterComponent,
  },
};
</script>

<style lang="scss" scoped>
#app {
  position: relative;
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
  gap: $big-gap;
  padding: 32px $mobile-padding;

  @media (min-width: $tablet-screen) {
    padding: 64px 128px;
  }
}
</style>
