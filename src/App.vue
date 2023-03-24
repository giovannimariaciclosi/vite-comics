<script>
import AppNavbar from "./components/AppNavbar.vue";
import AppContentSection from "./components/AppContentSection.vue";
import AppIconSection from "./components/AppIconSection.vue";

export default {
  data() {
    return {};
  },

  components: {
    AppNavbar,
    AppContentSection,
    AppIconSection,
  },
};
</script>

<template>
  <div>
    <AppNavbar></AppNavbar>
    <AppContentSection></AppContentSection>
    <AppIconSection></AppIconSection>
  </div>
</template>

<style lang="scss" scoped></style>
