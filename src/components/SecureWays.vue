<template>
  <section id="secure_section">
    <div class="secure_ways">
      <div class="row_secure">
        <div class="full_column">
          <h2>{{ HeadSection }}</h2>
          <div class="wrap_ways">
            <ul v-for="way in ways" :key="way.id">
              <li>
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
      HeadSection: "Ways we secure our site",
      ways: [
        {
          id: 1,
          name: "All communications are secured using strong encryption.",
          icon: require("@/assets/righticon.svg")
        },
        {
          id: 2,
          name: "Cross Site Request Forgery (CSRF) Protection",
          icon: require("@/assets/righticon.svg")
        },
        {
          id: 3,
          name: "Cross Site Scripting (XSS) Protection",
          icon: require("@/assets/righticon.svg")
        },
        {
          id: 4,
          name: "Advanced DDoS Attack Protection",
          icon: require("@/assets/righticon.svg")
        },
        {
          id: 5,
          name: "All data is stored in highly secure AWS data centers.",
          icon: require("@/assets/righticon.svg")
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
#secure_section {
  background-color: #297afb;
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
        color: #fff;
        font-size: 42px;
        line-height: 1.5;
        font-weight: 600;
        margin: 0;
        padding: 0;
      }

      .wrap_ways {
        max-width: 780px;
        margin: 0 auto;

        ul {
          padding: 0;
          margin: 0;

          li {
            list-style: none;
            border-bottom: 1px solid rgba(0, 0, 0, 0.1);
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;

            p {
              color: #fff;
              margin-right: 20px;
              font-size: 22px;
              line-height: 1.5;

              @media (max-width: 767px) {
                margin-right: 0;
                // font-size: 20px;
              }
            }

            img {
              @media (max-width: 400px) {
                // margin-top: 20px;
                // margin-left: 30px;
              }
            }
          }
        }
      }
    }
  }
}
</style>
