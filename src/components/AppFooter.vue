<script>
export default {
  data() {
    return {
      socialIcons: [
        "footer-facebook.png",
        "footer-twitter.png",
        "footer-youtube.png",
        "footer-pinterest.png",
        "footer-periscope.png",
      ],
    };
  },
};
</script>

<template>
  <div id="main-container">
    <div
      id="container-centered"
      class="d-flex justify-content-between align-items-center"
    >
      <button>SIGN-UP NOW!</button>
      <div class="social">
        <div class="social-text">FOLLOW US</div>
        <div class="social-icon-container">
          <img v-for="icon in socialIcons" :src="'/img/' + icon" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "../style.scss";
#main-container {
  background-color: #303030;
  color: white;

  #container-centered {
    @include containerCentered(1200px);
    padding: 1em 0;
    display: flex;
    gap: 40px;
    justify-content: center;

    button {
      padding: 8px 15px;
      background-color: transparent;
      border: 2px solid #0282f9;
      font-weight: bold;
    }

    .social {
      display: flex;
      align-items: center;
      gap: 30px;

      .social-text {
        color: #0282f9;
        font-weight: bold;
      }

      .social-icon-container {
        display: flex;
        gap: 15px;

        img {
          max-width: 30px;
        }
      }
    }
  }
}
</style>
