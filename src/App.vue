<template>
  <router-view />
</template>

<script>
export default {
  watch: {
    // change web-page title
    $route(to) {
      document.title = to.meta.title || "Main";
    },
  },
  created() {
    // change web-page title first load
    document.title = this.$route.meta.title || "Main";
  },
};
</script>

<style lang="scss"></style>
