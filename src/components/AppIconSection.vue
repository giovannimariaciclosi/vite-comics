<script>
export default {
  data() {
    return {
      iconsList: [
        {
          text: "DIGITAL COMICS",
          image: "buy-comics-digital-comics.png",
        },
        {
          text: "DC MERCHANDISE",
          image: "buy-comics-merchandise.png",
        },
        {
          text: "SUBSCRIPTION",
          image: "buy-comics-subscriptions.png",
        },
        {
          text: "COMIC SHOP LOCATOR",
          image: "buy-comics-shop-locator.png",
        },
        {
          text: "DC POWER VISA",
          image: "buy-dc-power-visa.svg",
        },
      ],
    };
  },
};
</script>

<template>
  <div id="main-container">
    <div id="container-centered">
      <div v-for="icon in iconsList" class="card-container">
        <img v-bind:src="'/img/' + icon.image" alt="Digital comics" />
        <div class="card-text">{{ icon.text }}</div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "../style.scss";

#main-container {
  background-color: #0282f9;
  color: white;

  #container-centered {
    @include containerCentered(1200px);
    padding: 2em 0;
    display: flex;
    gap: 40px;
    justify-content: center;
  }
  .card-container {
    display: flex;
    align-items: center;
    gap: 10px;
    min-width: 190px;

    img {
      max-width: 50px;
    }

    .card-text {
    }
  }
}
</style>
