<template>
  <section class="security">
    <div class="wrapper">
      <div class="full_column">
        <h2>{{ Stitle }}</h2>
        <p>{{ SubStitle }}</p>
        <a href>{{ linkName }}</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    Stitle: {
      type: String,
      required: true
    },
    SubStitle: {
      type: String,
      required: true
    },
    linkName: {
      type: String,
      required: true
    }
  }
};
</script>

<style lang="stylus" scoped>
.security {
  background-color: #297afb;
  padding: 100px 0;

  .wrapper {
    padding: 0 15px;
    margin: 0 auto;

    @media (min-width: 1140px) {
      max-width: 780px;
    }

    .full_column {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;

      h2 {
        color: #fff;
        font-size: 42px;
        line-height: 1.5;
        margin: 0 0 30px 0;
        padding: 0;
      }

      p {
        color: #d3e4fe;
        margin-top: 20px;
        font-size: 19px;
        line-height: 1.8;
        font-weight: 400;
        margin: 0;
        padding: 0;
      }

      a {
        margin-top: 40px !important;
        margin: 0;
        padding: 0;
        color: #fff;
        background-color: #01d8fd;
        display: inline-block;
        padding: 15px 20px;
        border-radius: 3px;
        font-size: 15px;
        box-shadow: 0 4px 6px rgba(50, 50, 93, 0.11), 0 1px 3px rgba(0, 0, 0, 0.08);
        text-decoration: none;
        cursor: pointer;
      }
    }
  }
}
</style>
