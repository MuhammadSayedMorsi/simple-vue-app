<template>
  <div id="app">
    <!-- <HeroSection/> -->
    <Hero
      HeroTitle="Payments made simple."
      HeroSubTitle="Accepting payments has never been this frictionless and fast."
      ButtonText="Sign up for free"
    />
    <Howworks title="How does it work for..."/>
    <section class="features">
      <div class="features_row">
        <div class="wrap_feature">
          <Features
            icon="ICON"
            headTitle="Payments Gateway"
            subTitle="We allow you to accept all major cards and accept payments through Apple Pay, Android Pay and Microsoft Pay. With no additional setup."
          />
        </div>
        <div class="wrap_feature">
          <Features
            icon="ICON"
            headTitle="Dynamic Notifications"
            subTitle="Just give us the details and we can automatically send instant SMS and or email notifications. All at no extra cost."
          />
        </div>
      </div>
      <div class="features_row">
        <div class="wrap_feature">
          <Features
            icon="ICON"
            headTitle="Reassuringly Secure"
            subTitle="We use industry leading technologies to ensure high levels of security all around. Your data is always safe with us."
          />
        </div>
        <div class="wrap_feature">
          <Features
            icon="ICON"
            headTitle="Simple and Intuitive"
            subTitle="We created SuperPay to be as easy to use as possible, from our Dashboard to Pay Area to emails. All are simple and easy to use."
          />
        </div>
      </div>
    </section>
    <Pricing/>
    <SecuritySection
      Stitle="Cutting edge Security."
      subSecurityTitle="Want to see just the few of the many things we do to achieve this?"
      linkName="Let me See"
    />
    <GetStarted/>
    <SignUp/>
    <Program/>
  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import Features from "./components/Features.vue";
import Pricing from "./components/Pricing.vue";
import SecuritySection from "./components/SecuritySection.vue";
import GetStarted from "./components/GetStarted.vue";
import SignUp from "./components/SignUp.vue";
import Howworks from "./components/Howworks.vue";
import Program from "./components/Program.vue";

// import HeroSection from "./components/HeroSection.vue";
// import click from "./components/click.vue";
export default {
  name: "app",
  components: {
    Hero,
    Howworks,
    Features,
    Pricing,
    SecuritySection,
    GetStarted,
    SignUp,
    Program
    // HeroSection
    // click
  }
};
</script>
<style lang="stylus" scoped>
// adjust the fonts for the app
@font-face {
  font-family: 'CircularStd-Book';
  src: url('./assets/fonts/CircularStd-Book.otf');
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'CircularStd-bold';
  src: url('./assets/fonts/CircularStd-Bold.otf');
  font-style: normal;
  font-display: swap;
}

body {
  font-family: 'CircularStd-Book', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 17px;
  font-weight: 400;
}

.features {
  background-color: #297afb;

  // padding: 100px 0;
  &_row {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    padding: 100px 15px;

    @media (min-width: 1140px) {
      max-width: 1020px;
    }

    @media (max-width: 767px) {
      flex-direction: column;
      text-align: center;
    }

    .wrap_feature {
      width: 50%;
      max-width: 50%;

      @media (max-width: 767px) {
        width: 100%;
        max-width: 100%;
      }
    }
  }
}
</style>

