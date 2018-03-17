<template>
  <div class="container">
    <div>
      <ToolBar></ToolBar>
      <nuxt></nuxt>
    </div>

  </div>
</template>

<script>
import ToolBar from "~/components/Toolbar.vue";
export default {
  components: {
    ToolBar
  }
};
</script>

<style>

</style>
