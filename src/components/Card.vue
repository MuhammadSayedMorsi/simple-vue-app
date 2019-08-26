<template>
  <div class="card" :style="{'z-index': '1'}">
    <!-- <div class="program__img" :style="{ backgroundImage: `url('${bgImg}')` }"></div> -->
    <div class="program_number">{{ NumberCard }}</div>
    <div class="program__content">
      <h3>{{ CardTitle }}</h3>
      <p>{{ CardSub }}</p>
      <a href>
        <span>{{ CardLink }}</span>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="20"
          height="20"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="btn__icon icon icon--sm"
        >
          <line x1="5" y1="12" x2="19" y2="12"></line>
          <polyline points="12 5 19 12 12 19"></polyline>
        </svg>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    bgImg: {
      type: String,
      required: true
    },
    CardTitle: {
      type: String,
      required: true
    },
    CardSub: {
      type: String,
      required: true
    },
    CardLink: {
      type: String,
      required: true
    },
    NumberCard: {
      type: String,
      required: true
    }
  }
};
</script>

<style lang="stylus" scoped>
.card {
  transition: all 0.3s ease-in-out;


  &:hover {
    .program_number, h3, a, p {
      color: #fff !important;
      transition: all 0.3s ease-in-out;
      border-color: #fff;
    }
  }
}

.program_number {
  font-size: 14px;
  line-height: 2.2rem;
  color: rgba(0, 0, 0, 0.4);
  z-index: 1;
}

.program__content {
  padding-left: 16px;
  z-index: 10;

  h3 {
    margin: 0;
    padding: 0;
    font-size: 24px;
    line-height: 3.2rem;
    margin: 0 0 20px;
    color: #252525;
    z-inde: 1;
    font-family: 'CircularStd-bold';

  }

  p {
    margin: 0;
    padding: 0;
    font-size: 16px;
    line-height: 2.3rem;
    color: rgba(0, 0, 0, 0.6);
    font-family: CircularStd-Book,sans-serif;

  }

  a {
    margin-top: 15px;
    background: transparent;
    border: 1px solid rgba(0, 0, 0, 0.05);
    color: #2c2c2c;
    padding: 10px;
    cursor: pointer;
    position: relative;
    overflow: hidden;
    font-size: 13px;
    line-height: 2.6rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    text-decoration: none;
    font-family: CircularStd-Book,sans-serif;

  }
}
</style>
