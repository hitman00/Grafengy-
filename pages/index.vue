<template>
  <div :class="$style.App">
    <div :class="$style.main">
      <Header />
      <BigImage />
      <Partners />
      <Slider />
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header/Header.vue'
import BigImage from '@/components/BigImage/BigImage.vue'
import Partners from '@/components/Partners/Partners.vue'
import Slider from '@/components/Slider/Slider.vue'
import Footer from '@/components/Footer/Footer.vue'
export default {
  components: {
    Header,
    BigImage,
    Partners,
    Slider,
    Footer,
  },
}
</script>

<style lang="scss" module>
.main {
  max-width: 1200px;
  padding-left: 15px;
  padding-right: 15px;
  margin: 0 auto;
}
</style>
