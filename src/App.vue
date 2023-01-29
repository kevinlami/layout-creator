<template>
  <HeaderLayout />
  <MenuLateral />
</template>

<script>
import HeaderLayout from "./components/HeaderLayout.vue";
import MenuLateral from "./components/MenuLateral.vue";

export default {
  name: "App",
  components: {
    HeaderLayout,
    MenuLateral,
  },
};
</script>

<style lang="scss">
@import "@/styles/styles.scss";
</style>
