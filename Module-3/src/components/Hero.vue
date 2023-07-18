<script setup>
  let hero = {
      imageSrc: "src/assets/images/market-launch-pana.svg",
      imageAlt: "Image",
      headingText: "Promote Your Products by Colorlib",
      excerptText: `Another cool free html css template by <a href="#" target="_blank" class="highlight">Colorlib</a> Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast`,
      seeFeaturesText: "See Features",
      pricingText: "Pricing",
      imageAnimation: "fade-right",
      headingAnimation: "fade-up",
      excerptAnimation: "fade-up",
      buttonsAnimation: "fade-up",
  }
</script>

<template>
  <div class="untree_co-hero" id="home-section">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-12">
          <div class="dots"></div>

          <div class="row align-items-center">
            <div class="col-lg-7 ml-auto order-lg-2" :data-aos="hero.imageAnimation" :data-aos-delay="400">
              <img :src="hero.imageSrc" :alt="hero.imageAlt" class="img-fluid">
            </div>

            <div class="col-lg-5">
              <h1 class="heading" :data-aos="hero.headingAnimation" :data-aos-delay="0">{{ hero.headingText }}</h1>

              <div class="excerpt" :data-aos="hero.excerptAnimation" :data-aos-delay="100">
                <p v-html="hero.excerptText"></p>
              </div>

              <p :data-aos="hero.buttonsAnimation" :data-aos-delay="200">
                <a href="#features-section" class="btn btn-primary smoothscroll">{{ hero.seeFeaturesText }}</a>
                <a href="#pricing-section" class="btn btn-outline-primary smoothscroll">{{ hero.pricingText }}</a>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>