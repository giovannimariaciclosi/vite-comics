<script>
import AppNavbar from "./components/AppNavbar.vue";
import AppContentSection from "./components/AppContentSection.vue";
import AppIconSection from "./components/AppIconSection.vue";
import AppLinkSection from "./components/AppLinkSection.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  data() {
    return {};
  },

  components: {
    AppNavbar,
    AppContentSection,
    AppIconSection,
    AppLinkSection,
    AppFooter,
  },
};
</script>

<template>
  <div>
    <AppNavbar></AppNavbar>
    <AppContentSection></AppContentSection>
    <AppIconSection></AppIconSection>
    <AppLinkSection></AppLinkSection>
    <AppFooter></AppFooter>
  </div>
</template>

<style lang="scss" scoped></style>
