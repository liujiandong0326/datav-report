<template>
  <div class="home">
    <top-view />
    <sales-view />
    <map-view />
    <bottom-view />
  </div>
</template>

<script>
import TopView from "@/components/TopView";
import SalesView from "@/components/SalesView";
import MapView from "@/components/MapView";
import BottomView from "@/components/BottomView";

export default {
  components: {
    TopView,
    SalesView,
    MapView,
    BottomView,
  },
};
</script>

<style lang="scss" scoped>
.home {
  width: 100%;
  height: 100%;
  padding: 20px;
  box-sizing: border-box;
  background: #eee;
}
</style>
