<template>
  <div class="app-wrapper">
    <SideBar class="sidebar-container"></SideBar>
  </div>
</template>

<script lang="ts">
import { computed, defineComponent } from "vue";
import SideBar from "@/components/side_bar/Index.vue";

export default defineComponent({
  name: "Layout",
  components: {
    SideBar,
  },
  setup() {
    return {};
  },
});
</script>

<style lang="scss" scoped>
.app-wrapper {
  @include clearfix;
  position: relative;
  height: 100%;
  width: 100%;
}
.sidebar-container {
  transition: width 0.28s;
  width: $sideBarWidth !important;
  height: 100%;
  position: fixed;
  font-size: 0px;
  top: 0;
  bottom: 0;
  left: 0;
  z-index: 1001;
  overflow: hidden;
  // background-color: #ffffff !important;
  background-color: pink;
}
</style>
