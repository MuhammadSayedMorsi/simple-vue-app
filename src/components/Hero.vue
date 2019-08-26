<template>
  <section class="hero_header">
    <div class="wrapper">
      <div class="hero_row">
        <div class="hero_content">
          <h1>{{ HeroTitle }}</h1>
          <p>{{ HeroSubTitle }}</p>
          <button>{{ ButtonText }}</button>
          <div class="phone_image">
            <div class="browser_phone">
              <div class="browser_phone_browser">
                <div class="mask">
                  <img :src="Demodasbord" alt>
                </div>
              </div>
              <div class="browser_iphone">
                <div class="mask">
                  <img :src="PaydemoSrc" alt>
                </div>
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
      Demodasbord: "https://superpay.it/media/images/demo-dashboard.png",
      PaydemoSrc: "https://superpay.it/media/images/pay-demo.png"
    };
  },
  props: {
    HeroTitle: {
      type: String,
      required: true
    },
    HeroSubTitle: {
      type: String,
      required: true
    },
    ButtonText: {
      type: String,
      required: true
    }
  }
};
</script>

<style lang="stylus" scoped>
.wrap_content_feature {
  .icon {
    background-color: #2898fb;
    width: 64px;
    height: 64px;
    flex-shrink: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    background: rgba(34, 126, 247, 0.07);
    margin-bottom: 20px;
    margin-right: 20px;
    color: #fff;
  }

  .feature_content {
    h1 {
      color: #fff;
      // color: red;
      font-size: 22px;
      line-height: 1.5;
      font-weight: 600;
      font-family: 'CircularStd-bold';


    }

    p {
      color: #d3e4fe;
      font-size: 19px;
      line-height: 1.8;
      font-weight: 400;
    }
  }
}

.hero_header {
  padding: 100px 0;
  overflow: hidden;
  position: relative;

  .wrapper {
    margin: 0 auto;
    padding: 0 15px;

    @media (min-width: 1140px) {
      width: 1140px;
    }

    .hero_row {
      .hero_content {
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        text-align: center;

        h1 {
          font-size: 55px;
          font-weight: 600;
          color: #000;
          line-height: 1.5;
          margin: 0;
          padding: 0;
          font-family: 'CircularStd-bold';
        }

        p {
          color: #8f8f8f;
          margin-top: 20px;
          font-size: 22px;
          line-height: 1.8;
          font-weight: 400;
          margin: 0;
          padding: 0;
          font-family: CircularStd-Book,sans-serif;
        }

        button {
          background-color: #297afb;
          outline: 0;
          border: 0;
          margin-top: 40px;
          color: #fff;
          padding: 15px 20px;
          border-radius: 3px;
          font-size: 15px;
          box-shadow: 0 4px 6px rgba(50, 50, 93, 0.11), 0 1px 3px rgba(0, 0, 0, 0.08);
          cursor: pointer;
          font-weight: bold;
          font-family: 'CircularStd-bold';
          
        }

        .phone_image {
          max-width: 1020px;
          position: relative;
          width: 100%;

          .browser_phone {
            position: relative;
            margin-top: 80px;

            .browser_phone_browser {
              border-radius: 6px;
              background-size: 60px;
              box-shadow: 0 10px 20px rgba(40, 39, 66, 0.06);
              overflow: hidden;
              width: 900px;
              z-index: 2;
              background-size: auto 30px;
              position: relative;
              box-shadow: 0 15px 19px 6px rgba(0, 0, 0, 0.05);

              &:before {
                content: '';
                height: 30px;
                line-height: 30px;
                display: block;
                width: 100%;
                position: relative;
                background: linear-gradient(-180deg, #fafbfc 0, #f1f4f7 100%);
              }

              &:after {
                content: '';
                width: 12px;
                height: 12px;
                background: #e2e5e5;
                position: absolute;
                border-radius: 50%;
                top: 10px;
                left: 8px;
                box-shadow: 18px 0 0 #e2e5e5, 36px 0 0 #e2e5e5;
              }

              .mask {
                min-height: 490px;
                max-height: 580px;
                width: 100%;
                overflow: hidden;
                border-radius: 0 0 4px 4px;
                background: #fff;
                position: relative;

                img {
                  width: 100%;
                  display: block;
                  z-index: 2;
                  position: relative;
                }
              }
            }

            .browser_iphone {
              z-index: 2;
              position: absolute;
              display: inline-block;
              bottom: 0;
              right: 0;
              background: linear-gradient(#f4f4f4, #f2f2f2);
              box-shadow: inset 0 0 1px 1px #dbdcdd, inset 0 0 1px 4px #efefef, inset 0 0 0 5px #fff, inset 0 0 0 6.5px #edf1f2, inset 5px 0 7px 5px #fff, inset -5px 0 7px 5px #fff;
              border-radius: 35px;
              padding: 50px 15px 60px;

              &:before {
                content: '';
                width: 52px;
                height: 7px;
                border-radius: 10px;
                position: absolute;
                box-shadow: inset 0 4px 3px 0 #e6e6e6, inset 0 0 0 2px #ececec;
                top: 25px;
                left: calc(50% - 26px);
              }

              &:after {
                content: '';
                width: 38px;
                height: 38px;
                border-radius: 50%;
                position: absolute;
                box-shadow: inset 0 -2px 0.2px 0 #d5d5d5, inset 0 0 0 2.5px #e8e8e8;
                bottom: 14px;
                left: calc(50% - 19px);
              }

              .mask {
                width: 210px;
                min-height: 310px;
                max-height: 400px;
                overflow: hidden;
                border-radius: 0 0 4px 4px;
                background: #fff;
                position: relative;

                img {
                  width: 100%;
                  display: block;
                  z-index: 2;
                  position: relative;
                }
              }
            }
          }
        }
      }
    }
  }
}
</style>
