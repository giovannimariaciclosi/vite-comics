<script>

export default {
  name: "AppCard",
  data() {
  },

  props: {

    thumb: String,
    series: String,
  },
}

</script>

<template>
  <div class="card">
    <img class="thumb" :src="thumb" :alt="series">
    <div class="series">{{ series }}</div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  max-width: 180px;
  background-color: #1c1c1c;
  padding-top: 2em;
  border: none;
  cursor: pointer;


  .thumb {
    width: 100%;
  }

  .series {
    padding-top: .8em;
    text-transform: uppercase;
    font-size: .8em;
  }
}
</style>