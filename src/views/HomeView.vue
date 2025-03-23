<script lang="ts" setup>
import TheHeader from "@/components/TheHeader.vue";
import TheMain from "@/components/TheMain.vue";
import TheFooter from "@/components/TheFooter.vue";

defineOptions({
  name: "HomeView",
});
</script>

<template>
  <div class="home-view">
    <TheHeader />
    <TheMain />
    <TheFooter />
  </div>
</template>

<style lang="scss" scoped>
.home-view {
}
</style>
