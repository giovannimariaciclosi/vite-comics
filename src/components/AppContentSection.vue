<script>
export default {
  data() {
    return {};
  },
};
</script>

<template>
  <div id="main-container">
    <div id="container-centered">Content goes here</div>
  </div>
</template>

<style lang="scss" scoped>
@import "../style.scss";

#main-container {
  background-color: #1c1c1c;
  color: white;

  #container-centered {
    @include containerCentered(1200px);
    font-size: 2em;
    padding: 2em 0;
  }
}
</style>
