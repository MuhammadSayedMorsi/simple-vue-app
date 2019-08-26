<template>
  <div class="wrap_content_feature">
    <div class="icon">
      <img :src="imgSrcFeautre" alt>
    </div>
    <div class="feature_content">
      <h1>{{ headTitle }}</h1>
      <p>{{ subTitle }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgSrcFeautre: require("@/assets/iconfeature.svg")
    };
  },
  props: {
    icon: {
      type: String,
      required: true
    },
    headTitle: {
      type: String,
      required: true
    },
    subTitle: {
      type: String,
      required: true
    }
  }
};
</script>

<style lang="stylus" scoped>
.wrap_content_feature {
  display: flex;
  justify-content: center;
  align-items: start;

  @media (max-width: 767px) {
    flex-direction: column;
    // text-align: center;
    align-items: center;
  }

  .icon {
    background-color: #2898fb;
    width: 64px;
    height: 64px;
    flex-shrink: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    margin-bottom: 20px;
    margin-right: 20px;

    img {
      width: 100%;
      max-width: 30px;
      max-height: 30px;
    }
  }

  .feature_content {
    h1 {
      font-size: 22px;
      line-height: 1.5;
      color: #fff;
      font-weight: 600;
      margin: 0;
      padding: 0;
    }

    p {
      font-size: 19px;
      line-height: 1.8;
      font-weight: 400;
      color: #fff;
      max-width: 380px;
    }
  }
}
</style>
