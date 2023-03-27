<script>
export default {
  data() {
    return {
      linksList: [
        {
          title: "DC COMICS",
          contents: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },
        {
          title: "SHOP",
          contents: ["Shop DC", "Shop DC Collectibles"],
        },
        {
          title: "DC",
          contents: [
            "Terms Of Use",
            "Privacy Policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          title: "SITES",
          contents: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
      ],
    };
  },
};
</script>

<template>
  <div id="main-container">
    <div id="container-centered">
      <div class="list-container">
        <div class="list-title">{{ linksList[0].title }}</div>
        <ul class="list">
          <li v-for="(link, index) in linksList[0].contents">
            {{ link }}
          </li>
        </ul>
        <div class="list-title">{{ linksList[1].title }}</div>
        <ul class="list">
          <li v-for="(link, index) in linksList[1].contents">
            {{ link }}
          </li>
        </ul>
      </div>
      <div class="list-container">
        <div class="list-title">{{ linksList[2].title }}</div>
        <ul class="list">
          <li v-for="(link, index) in linksList[2].contents">
            {{ link }}
          </li>
        </ul>
      </div>
      <div class="list-container">
        <div class="list-title">{{ linksList[3].title }}</div>
        <ul class="list">
          <li v-for="(link, index) in linksList[3].contents">
            {{ link }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "../style.scss";

#main-container {
  color: white;
  background-image: url("/img/footer-bg.jpg");
  min-height: 370px;
  background-repeat: no-repeat;
  background-size: cover;

  #container-centered {
    @include containerCentered(1200px);
    background-image: url("/img/dc-logo-bg.png");
    background-repeat: no-repeat;
    background-position: right;

    display: flex;
    gap: 50px;

    min-height: 370px;
    padding: 2em 0;

    .list-container {
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;

      .list-title {
        font-size: 1.2em;
        font-weight: bold;
        padding-bottom: 0.6em;
      }

      .list {
        color: #959595;
        padding-bottom: 0.6em;
        font-size: 0.8em;

        li {
          cursor: pointer;
        }
      }
    }
  }
}
</style>
