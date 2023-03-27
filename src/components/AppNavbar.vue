<script>
export default {
  data() {
    return {
      linksList: [
        "CHARACTERS",
        "COMICS",
        "MOVIES",
        "TV",
        "GAMES",
        "COLLECTIBLES",
        "VIDEOS",
        "FANS",
        "NEWS",
        "SHOP",
      ],
    };
  },
};
</script>

<template>
  <div id="navbar-container" class="d-flex justify-content-between align-items-center">
    <div class="img-container">
      <img src="/img/dc-logo.png" alt="DC Logo" />
    </div>
    <ul class="d-flex align-items-center">
      <li v-for="link in linksList">{{ link }}</li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
@import "../style.scss";

#navbar-container {
  @include containerCentered(1200px);

  .img-container {
    padding: 1em 0;
  }
}

ul {
  gap: 20px;
  font-weight: bold;

  li {
    cursor: pointer;
    position: relative;

    &:hover::after {
      content: "";
      height: 6px;
      position: absolute;
      left: 0;
      right: 0;
      top: 74px;
      width: 100%;
      background: #0282f9;
    }

    &:active::after {
      content: "";
      height: 6px;
      position: absolute;
      left: 0;
      right: 0;
      top: 74px;
      width: 100%;
      background: #0282f9;
    }
  }
}
</style>
