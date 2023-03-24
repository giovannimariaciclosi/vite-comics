<script>
export default {
  data() {
    return {};
  },
};
</script>

<template>
  <div id="section-container">Content goes here</div>
</template>

<style lang="scss" scoped>
@mixin containerCentered($bgcolor, $maxwidth) {
  max-width: $maxwidth;
  background-color: $bgcolor;
  margin: 0 auto;
  padding: 0 0.5em;
}

#section-container {
  @include containerCentered(#1c1c1c, 1200px);
}
</style>
