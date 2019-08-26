<template>
  <section class="how_works">
    <div class="wrapper">
      <div class="full_column">
        <h2>{{ Title }}</h2>
        <div class="button" :class="showCase" @click.prevent>
          <button class="button_one content_1" @click="makeActive('content_1')">Payment Links</button>
          <button class="button_two content_2" @click="makeActive('content_2')">Payment Requests</button>
        </div>
      </div>
      <div class="hold_content">
        <div class="wrap_content_1" v-if="showCase === 'content_1'">
          <div class="coll_4">
            <div class="card">
              <img :src="cardImg" alt>
              <div class="card_content">
                <h3>1. Create and share</h3>
                <p>Within your Dashboard you can create multiple payment links and share with anyone.</p>
              </div>
            </div>
          </div>
          <div class="coll_4">
            <div class="card">
              <img :src="cardImg" alt>
              <div class="card_content">
                <h3>1. Create and share</h3>
                <p>Within your Dashboard you can create multiple payment links and share with anyone.</p>
              </div>
            </div>
          </div>
          <div class="coll_4">
            <div class="card">
              <img :src="cardImg" alt>
              <div class="card_content">
                <h3>1. Create and share</h3>
                <p>Within your Dashboard you can create multiple payment links and share with anyone.</p>
              </div>
            </div>
          </div>
        </div>
        <div class="wrap_content_2" v-if="showCase === 'content_2'">
          <div class="coll_4">
            <div class="card">
              <img :src="cardImgTwo" alt>
              <div class="card_content">
                <h3>1.Create a request</h3>
                <p>Within your Dashboard you can create multiple payment links and share with anyone.</p>
              </div>
            </div>
          </div>
          <div class="coll_4">
            <div class="card">
              <img :src="cardImg" alt>
              <div class="card_content">
                <h3>2. Send link</h3>
                <p>Within your Dashboard you can create multiple payment links and share with anyone.</p>
              </div>
            </div>
          </div>
          <div class="coll_4">
            <div class="card">
              <img :src="cardImgTwo" alt>
              <div class="card_content">
                <h3>3. Payment</h3>
                <p>Within your Dashboard you can create multiple payment links and share with anyone.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      showCase: "content_1",
      show: false,
      cardImg:
        "https://superpay.it/media/images/create-reusable-payment-link-v2.png",
      cardImgTwo: "https://superpay.it/media/images/pay-request-img3.jpg"
    };
  },
  methods: {
    makeActive: function(item) {
      this.showCase = item;
    }
  },
  props: {
    Title: {
      type: String,
      required: true
    }
  }
};
</script>

<style lang="stylus" scoped>
.content_1 .content_1, .content_2 .content_2 {
  background-color: #007BFF;
  // font-size: 50px;
}

.how_works {
  padding: 100px 0;
  overflow: hidden;
  position: relative;

  .wrapper {
    margin: 0 auto;
    padding: 0 15px;

    @media (min-width: 1200px) {
      width: 1140px;
    }

    .full_column {
      width: 100%;
      margin: 0 auto;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;

      h2 {
        font-size: 42px;
        line-height: 1.5;
        font-weight: 600;
        margin: 0;
        padding: 0;
        font-family: 'CircularStd-bold';


        @media (max-width: 767px) {
          font-size: 30px;
        }
      }

      .button {
        margin-top: 25px;
        display: flex;
        justify-content: center;


        button {
          display: inline-block;
          border-radius: 8px;
          color: white;
          padding: 13px 10px 13px;
          font-size: 15px;
          margin: 5px;
          border: 1px solid #007BFF;
          width: 200px;
          background-color: transparent;
          outline: none;
          color: #007BFF;
          cursor: pointer;
          transition: all 0.3s ease-in-out;
          font-family: CircularStd-Book,sans-serif;


          @media (max-width: 767px) {
            width: 150px;
          }
        }
      }
    }

    .hold_content {
      .wrap_content_1, .wrap_content_2 {
        display: flex;
        justify-content: center;
        align-items: center;

        @media (max-width: 767px) {
          flex-direction: column;
        }

        .coll_4 {
          flex-basis: 33.333333%;
          max-width: 33.333333%;
          margin-top: 40px;
          margin-right: 10px;

          @media (max-width: 767px) {
            flex-basis: 100%;
            max-width: 100%;
            margin-bottom: 30px;
          }

          .card {
            padding: 30px;
            min-height: 460px;
            border-radius: 3px;

            img {
              max-with: 100%;
              width: 100%;
            }

            .card_content {
              h3 {
                font-size: 22px;
                line-height: 1.5;
                margin: 0;
                padding: 0;
                font-family: 'CircularStd-bold';

              }

              p {
                margin-top: 20px;
                font-size: 19px;
                line-height: 1.8;
                font-weight: 400;
                font-family: CircularStd-Book,sans-serif;

              }
            }
          }
        }
      }
    }
  }
}

.content_1 .content_1, .content_2 .content_2 {
  background-color: #007BFF !important;
  color: #fff !important;
  border: 0;
  // font-size: 50px;
}
</style>
