<script>
import AppNavbar from "./components/AppNavbar.vue";
import AppContentSection from "./components/AppContentSection.vue";

export default {
  data() {
    return {};
  },

  components: {
    AppNavbar,
    AppContentSection,
  },
};
</script>

<template>
  <div>
    <AppNavbar></AppNavbar>
    <AppContentSection></AppContentSection>
  </div>
</template>

<style lang="scss" scoped></style>
