<template>
  <section class="pricing">
    <div class="wrapper">
      <div class="full_column">
        <h2>{{ priceHead }}</h2>
        <p>{{ subPriceTitl }}</p>
      </div>
      <div class="pricing_row">
        <div class="column_one">
          <div class="content_list">
            <h4>{{ headListone }}</h4>
            <div class="bold">
              <h6>
                1%
                <a href target="_blank">
                  <span>+ Stripe fee</span>
                </a>
              </h6>
            </div>
            <ul>
              <li v-for="list in lists" :key="list.id">
                <i>
                  <img :src="list.icon" alt>
                </i>
                <span>{{ list.name }}</span>
              </li>
            </ul>
            <a
              href
              style="background-color: #297afb; color: #fff;"
              class="link"
            >Sign up your business</a>
          </div>
        </div>

        <div class="column_one bg_color">
          <div class="content_list">
            <h4 style="color: #fff;">{{ headListTwo }}</h4>
            <div class="bold">
              <h6>
                <b style="color: #fff;">Custom</b>
                <span class="d_block">Process over £5,000 per month?</span>
              </h6>
            </div>
            <ul>
              <li v-for="list in lists" :key="list.id">
                <i>
                  <img :src="list.icon" alt>
                </i>
                <span class="colored_one">{{ list.name }}</span>
              </li>
            </ul>
            <a href style="background-color: #fff; color: #297afb;" class="link">Contact Us</a>
          </div>
        </div>
      </div>
      <div class="last_full_column">
        <a href>
          <img :src="logoSite" alt>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      priceHead: "We believe in simple and transparent pricing.",
      subPriceTitl: "Always know what you’ll pay.",
      headListone: "Per transaction",
      headListTwo: "Enterprise",
      logoSite: "https://superpay.it/media/images/stripe-v-dard.png",
      lists: [
        {
          id: 1,
          name:
            "Accept all major cards and payments through Apple Pay, Android Pay and Microsoft Pay.",
          icon: require("@/assets/rightcoloricon.svg")
        },
        {
          id: 2,
          name: "No charges for failed transactions",
          icon: require("@/assets/rightcoloricon.svg")
        },
        {
          id: 3,
          name: "SMS and email notifications",
          icon: require("@/assets/rightcoloricon.svg")
        },
        {
          id: 4,
          name: "Add Unlimited Team Members",
          icon: require("@/assets/rightcoloricon.svg")
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
.pricing {
  padding: 100px 0;
  background-color: #fff;

  .wrapper {
    padding: 0 15px;
    margin: 0 auto;

    @media (min-width: 1140px) {
      max-width: 780px;
    }

    .full_column {
      max-width: 780px;
      margin: 0 auto;
      text-align: center;

      h2 {
        color: #000;
        font-size: 42px;
        line-height: 1.5;
        font-weight: 600;
        margin: 0;
        padding: 0;
        font-family: 'CircularStd-bold';

      }

      p {
        font-size: 19px;
        line-height: 1.8;
        font-weight: 400;
        margin-top: 20px;
        color: #8f8f8f;
        font-family: CircularStd-Book,sans-serif;

      }
    }

    .pricing_row {
      margin-top: 75px;
      max-width: 780px;
      display: flex;
      justify-content: center;
      align-items: center;

      @media (max-width: 767px) {
        flex-direction: column;
      }

      .column_one {
        padding: 30px;
        display: flex;
        justify-content: space-between;
        flex-direction: column;
        flex-basis: 50%;
        max-width: 50%;

        @media (max-width: 767px) {
          flex-basis: 100%;
          max-width: 100%;
        }

        .content_list {
          margin-bottom: 20px;

          h4 {
            color: #000;
            font-size: 22px;
            line-height: 1.5;
            margin: 0;
            padding: 0;
            font-family: 'CircularStd-bold';

          }

          .bold {
            h6 {
              font-size: 50px;
              color: #000;
              line-height: 1.5;
              font-weight: 600;
              margin: 0;
              padding: 0;
              font-family: 'CircularStd-bold';


              a {
                text-decoration: none;
                color: #000;
                font-family: CircularStd-Book,sans-serif;


                span {
                  font-size: 20px;
                }
              }
            }
          }

          ul {
            margin: 0;
            padding: 0;

            li {
              list-style: none;
              margin-bottom: 20px;
              display: flex;
              justify-content: center;
              align-items: center;

              i {
                margin-right: 20px;
                width: 10%;
                max-width: 10%;
              }

              span {
                width: 90%;
                max-width: 90%;
                color: #8f8f8f;
                font-size: 15px;
                line-height: 1.5;
          font-family: CircularStd-Book,sans-serif;
                
              }
            }
          }
        }
      }

      .bg_color {
        background-color: #297afb;
        border-radius: 5px;

        .d_block {
          display: block;
          font-size: 19px;
          line-height: 1.8;
          font-weight: 400;
          color: #d3e4fe;
        }

        ul {
          li {
            .colored_one {
              color: #d3e4fe !important;
              font-size: 15px !important;
              line-height: 1.5 !important;
            }
          }
        }
      }
    }

    .last_full_column {
      margin-top: 60px;
      text-align: center;
    }
  }

  .link {
    width: 75%;
    margin: 0;
    text-align: center;
    display: inline-block;
    padding: 15px 20px;
    border-radius: 3px;
    font-size: 15px;
    box-shadow: 0 4px 6px rgba(50, 50, 93, 0.11), 0 1px 3px rgba(0, 0, 0, 0.08);
    text-decoration: none;
    background: #fff;
    color: #000;
    white-space: nowrap;
    border: none;
    -webkit-appearance: none;
    cursor: pointer;
  }
}
</style>
