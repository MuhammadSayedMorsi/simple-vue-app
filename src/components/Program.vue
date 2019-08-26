<template>
  <section class="main_grid_program">
    <div class="wrapper">
      <div class="row__grid__program">
        <div class="gird">
          <div class="column_one">
            <div class="wrap__content">
              <div
                class="program__img"
                :style="{'background-image': `url(${require('@/assets/undergraduate-card.svg')})`}"
              ></div>

              <Card
                CardTitle="Undergraduate"
                CardSub="Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus eveniet."
                CardLink="Undergraduate program at Hult"
                NumberCard="01"
              />
            </div>
          </div>

          <div class="column_one">
            <div class="wrap__content">
              <div
                class="program__img"
                :style="{'background-image': `url(${require('@/assets/masters-card.svg')})`, 'background-position': '-2500px', 'background-size': '5000%'}"
              ></div>

              <Card
                CardTitle="Undergraduate"
                CardSub="Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus eveniet."
                CardLink="Undergraduate program at Hult"
                NumberCard="02"
              />
            </div>
          </div>

          <div class="column_one">
            <div class="wrap__content">
              <div
                class="program__img"
                :style="{'background-image': `url(${require('@/assets/mba-card.svg')})`, 'background-size': '800%', 'background-position': '-2200px -1000px'}"
              ></div>

              <Card
                CardTitle="Undergraduate"
                CardSub="Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus eveniet."
                CardLink="Undergraduate program at Hult"
                NumberCard="03"
              />
            </div>
          </div>
          <div class="column_one">
            <div class="wrap__content">
              <div
                class="program__img"
                :style="{'background-image': `url(${require('@/assets/emba-card.svg')})`, 'background-size': '300%'}"
              ></div>

              <Card
                CardTitle="Undergraduate"
                CardSub="Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus eveniet."
                CardLink="Undergraduate program at Hult"
                NumberCard="04"
              />
            </div>
          </div>
          <div class="column_one">
            <div class="wrap__content">
              <div
                class="program__img"
                :style="{'background-image': `url(${require('@/assets/emba_v2-card-sb.svg')})`, 'background-size': '300%'}"
              ></div>

              <Card
                CardTitle="Undergraduate"
                CardSub="Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus eveniet."
                CardLink="Undergraduate program at Hult"
                NumberCard="05"
              />
            </div>
          </div>
          <div class="column_one">
            <div class="wrap__content">
              <div
                class="program__img"
                :style="{'background-image': `url(${require('@/assets/ashridge-card.svg')})`, 'background-size': '300%'}"
              ></div>

              <Card
                CardTitle="Undergraduate"
                CardSub="Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus eveniet."
                CardLink="Undergraduate program at Hult"
                NumberCard="06"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Card from "./Card.vue";
export default {
  components: {
    Card
  }
};
</script>

<style lang="stylus" scoped>
.main_grid_program {
  margin: 100px 0;
  overflow: hidden;

  .wrapper {
    margin: 0 auto;
    padding: 15px;
    @media (min-width: 1200px) {
      width: 1140px;
    }

    .row__grid__program {
      .gird {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;

        @media (max-width: 767px) {
          flex-direction: column;
        }

        .column_one {
          width: 32.4%;
          margin-right: 10px;
          box-shadow: 0 4px 4px 0 rgba(0,0,0,.2);
          // box-shadow: 0 4px 9px 0 rgba(0,0,0,.2);

          margin-bottom: 10px;
          transiton: all .3s ease-in-out;
          &:hover {
            box-shadow: none;
          }

          @media (max-width: 767px) {
            width: 100%;
            margin-bottom: 30px;
          }

          .wrap__content {
            overflow: hidden;
            position: relative;
            // border: 1px solid #fbf3e8;
            border: 1px solid rgba(0, 0, 0, 0.05);

            display: flex;
            flex-direction: column;
            background-color: #fff;
            padding: 50px;
            transition: all 0.3s ease-in-out;

            @media (max-width: 767px) {
              padding: 19px;
            }

            &:hover {
              cursor: pointer;

              h3, p, a {
                color: #fff !important;
              }
            }

            // StyleForImages
            .program__img {
              position: absolute;
              left: 0;
              top: 0;
              width: 100%;
              background-position: 50%;
              background-repeat: no-repeat;
              background-size: 200%;
              height: 100%;
              transition: all 0.3s ease-in-out;

              @media (min-width: 767px) {
                opacity: 0;
              }
            }
          }

          &:hover {
            .program__img {
              opacity: 1;
            }
          }
        }
      }
    }
  }
}
</style>
