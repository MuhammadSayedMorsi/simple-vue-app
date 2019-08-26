<template>
  <section id="secure_section">
    <div class="secure_ways">
      <div class="row_secure">
        <div class="full_column">
          <h2>{{ HeadSection }}</h2>
          <p>{{ subHeadSection }}</p>
          <div class="wrap_ways">
            <ul>
              <li v-for="way in ways" :key="way.id">
                <p>{{ way.name }}</p>
                <img :src="way.icon">
              </li>
            </ul>
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
      HeadSection: "How to get started",
      subHeadSection: "Start accepting payments in under 10 minutes",
      ways: [
        {
          id: 1,
          name: "Create a SuperPay account",
          icon: require("@/assets/rightcoloricon.svg")
        },
        {
          id: 2,
          name: "Enter bank details to receive payments",
          icon: require("@/assets/rightcoloricon.svg")
        },
        {
          id: 3,
          name: "Start accepting payments straight away",
          icon: require("@/assets/rightcoloricon.svg")
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
#secure_section {
  margin: 100px 0;

  .secure_ways {
    padding-top: 100px;

    .full_column {
      display: flex;
      justify-content: center;
      flex-direction: column;
      align-items: column;
      margin: 0 auto;
      text-align: center;

      h2 {
        color: #000;
        font-size: 42px;
        line-height: 1.5;
        font-weight: 600;
        margin: 0;
        padding: 0;
      }

      p {
        color: #8f8f8f;
        margin-top: 20px;
        font-size: 22px;
        line-height: 1.8;
        font-weight: 400;
      }

      .wrap_ways {
        max-width: 780px;

        @media (min-width: 1200px) {
          margin: 0 300px;
        }

        ul {
          padding: 0;
          margin: 0;

          li {
            list-style: none;
            border-bottom: 1px solid rgba(0, 0, 0, 0.1);
            padding: 20px;
            display: flex;
            justify-content: space-between;

            p {
              color: #000;
              margin-right: 20px;
              font-size: 22px;
              line-height: 1.5;

              @media (max-width: 767px) {
                margin-right: 0;
                width: 90%;
                max-width: 90%;
                // font-size: 20px;
              }
            }

            img {
              @media (max-width: 400px) {
                width: 10%;
                max-width: 10%;
              }
            }
          }
        }
      }
    }
  }
}
</style>
