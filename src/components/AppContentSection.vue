<script>
import AppCard from './AppCard.vue';

export default {
  data() {
    return {
      comics: [
        {
          "thumb": "https://imgix-media.wbdndc.net/asset/comics.series/ccd62cd2-c2f3-47ce-939d-aed6fd4e395b/5c74105a/box.jpg?w=200&h=200&",
          "price": "$19.99",
          "series": "Action Comics",
          "type": "comic book"
        },
        {
          "thumb": "https://imgix-media.wbdndc.net/asset/comics.series/5234b3c5-347b-45d6-aeb6-351fccc2fe9f/5f774f7c/box.jpg?w=200&h=200&",
          "price": "$3.99",
          "series": "American Vampire 1976",
          "type": "comic book"
        },
        {
          "thumb": "https://imgix-media.wbdndc.net/asset/comics.series/81b226d9-7420-49ee-ae8f-154961736f3c/5ce31251/box.jpg?w=200&h=200&",
          "price": "$16.99",
          "series": "Aquaman",
          "type": "graphic novel"
        },
        {
          "thumb": "https://imgix-media.wbdndc.net/asset/comics.series/9e59763d-6767-4102-a3a2-a39ba233c72f/3dd3d8f/box.jpg?w=200&h=200&",
          "price": "$2.99",
          "series": "Batgirl",
          "type": "comic book"
        },
        {
          "thumb": "https://imgix-media.wbdndc.net/asset/comics.series/b465f1d8-d118-47cb-b1ac-3e5a70659eea/e818ce/box.jpg?w=200&h=200&",
          "price": "$3.99",
          "series": "Batman",
          "type": "comic book"
        },
        {
          "thumb": "https://imgix-media.wbdndc.net/asset/comics.series/1e7c18b1-324c-49d9-9a9a-3a674206a42a/5cc88ed0/box.jpg?w=200&h=200&",
          "price": "$2.99",
          "series": "Batman Beyond",
          "type": "comic book"
        },
        {
          "thumb": "https://imgix-media.wbdndc.net/asset/comics.series/1e7c18b1-324c-49d9-9a9a-3a674206a42a/5cc88ed0/box.jpg?w=200&h=200&",
          "price": "$3.99",
          "series": "Batman/Superman",
          "type": "comic book"
        },
        {
          "thumb": "https://imgix-media.wbdndc.net/asset/comics.series/944de017-6398-4c5f-812b-3b75c1d6fbcf/39daf1a/box.jpg?w=200&h=200&",
          "price": "$4.99",
          "series": "Batman/Superman Annual",
          "type": "comic book"
        },
        {
          "thumb": "https://imgix-media.wbdndc.net/asset/comics.series/426ed7b5-a878-4454-b714-babaa0e06dfc/5b92dfa/box.jpg?w=200&h=200&",
          "price": "$5.99",
          "series": "Batman: The Joker War Zone",
          "type": "comic book"
        },
        {
          "thumb": "https://imgix-media.wbdndc.net/asset/comics.series/df79c31c-cd37-4ebc-a9c4-255cfb007802/5f43e23e/box.jpg?w=200&h=200&",
          "price": "$6.99",
          "series": "Batman: Three Jokers",
          "type": "comic book"
        },
        {
          "thumb": "https://imgix-media.wbdndc.net/asset/comics.series/426ed7b5-a878-4454-b714-babaa0e06dfc/5b92dfa/box.jpg?w=200&h=200&",
          "price": "$4.99",
          "series": "Batman: White Knight Presents: Harley Quinn",
          "type": "comic book"
        },
        {
          "thumb": "https://imgix-media.wbdndc.net/asset/comics.series/49b9cd78-45ca-4cbd-a2d5-e2469202a5d5/44058/box.jpg?w=200&h=200&",
          "price": "$16.99",
          "series": "Catwoman",
          "type": "graphic novel"
        }
      ],
    };
  },
  components: { AppCard }
};
</script>

<template>
  <div id="main-container">
    <div class="jumbotron">
    </div>
    <div id="container-centered">
      <div class="current-btn">Current Series</div>

      <AppCard v-for="comic in comics" :thumb="comic.thumb" :series="comic.series"></AppCard>

      <div class="load-more-btn">Load More</div>

    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "../style.scss";

#main-container {
  background-color: #1c1c1c;
  color: white;

  .jumbotron {
    height: 300px;
    background-image: url('/img/jumbotron.jpg');
    background-size: cover;
  }

  #container-centered {
    @include containerCentered(1200px);
    padding: 2em 0;
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    gap: 20px;
    position: relative;

    .current-btn {
      @include button(#0282f9);
      font-size: 1.2em;
      position: absolute;
      z-index: 2;
      top: -22px;
      left: 0;
    }

    .load-more-btn {
      @include button(#0282f9);
      padding: 0.8em 5em;
      margin-top: 2em;
      font-size: .8em;
    }
  }
}
</style>
