<template>
  <section class="section">
    <div class="wrapper">
      <div class="row_hero">
        <div class="column_1">
          <div class="wrap_text">
            <h1>{{ SecurityTitle }}</h1>
            <p>{{ SecurityText }}</p>
          </div>
        </div>
        <div class="column_2">
          <div class="wrap_img">
            <img :src="ImgSecuritySrc" alt>
          </div>
        </div>
      </div>
    </div>
    <SecureWays/>
  </section>
</template>

<script>
import SecureWays from "./SecureWays.vue";
export default {
  data() {
    return {
      SecurityTitle: "Security",
      SecurityText:
        "We use a wide range of technologies to ensure high levels of security throughout the whole site.",
      ImgSecuritySrc: "https://superpay.it/media/images/secure.svg"
    };
  },
  components: {
    SecureWays
  }
};
</script>

<style lang="stylus" scoped>
.section {
  padding: 100px 0 0;

  .wrapper {
    margin: 0 auto;
    padding: 0 15px;

    @media (min-width: 1200px) {
      width: 1140px;
    }

    .row_hero {
      display: flex;
      justify-content: center;
      align-items: center;

      @media (max-width: 767px) {
        flex-direction: column;
      }

      .column_1 {
        margin-bottom: 40px;
        padding: 0 20px;
        width: 50%;

        @media (max-width: 767px) {
          width: 100%;
        }

        h1 {
          color: #000;
          font-size: 56px;
          line-height: 1.38;
          margin: 0;
          padding: 0;
        }

        p {
          color: #8f8f8f;
          margin-top: 20px;
          font-size: 22px;
          line-height: 1.8;
          font-weight: 400;
          width: 450px;

          @media (max-width: 767px) {
            width: 100%;
          }
        }
      }

      .column_2 {
        width: 50%;

        @media (max-width: 767px) {
          width: 100%;
        }

        .wrap_img {
          img {
            max-width: 100%;
          }
        }
      }
    }
  }
}
</style>
