<template>
  <div class="app-wrapper">
    <layout-left />
    <div class="app-container">
      <nav-bar />
      <app-main />
    </div>
  </div>
</template>

<script lang="ts">
import NavBar from "@/layout/components/NavBar.vue";
import AppMain from "@/layout/components/AppMain.vue";
import LayoutLeft from "@/layout/components/LayoutLeft.vue";
export default {
  name: "Layout",
  components: { LayoutLeft, AppMain, NavBar },
};
</script>

<style lang="scss" scoped>
.app-wrapper {
  width: 100vw;
  height: 100vh;
  display: flex;
  .app-container {
    flex: 1;
  }
}
</style>
