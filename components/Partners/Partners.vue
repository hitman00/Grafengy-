<template>
  <div :class="$style.partners_main">
    <div :class="$style.title">PARTNERS</div>
    <div :class="$style.box_image">
      <div v-for="(i, id) in list" :key="id" :class="$style.social">
        <img :src="i" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Partners',
  data: () => ({
    list: [
      require('@/assets/imgs/logitech.png'),
      require('@/assets/imgs/google.png'),
      require('@/assets/imgs/facebook.png'),
      require('@/assets/imgs/linkedIn.png'),
      require('@/assets/imgs/philips.png'),
    ],
  }),
}
</script>

<style lang="scss" module>
.partners_main {
}

.title {
  color: #969696;
  font-size: 16px;
  padding: 4% 0;
}

.box_image {
  display: flex;
  justify-content: space-between;
}

.social {
  position: relative;
  width: 13%;

  &:before {
    content: '';
    display: block;
    padding-bottom: 33%;
  }
  img {
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    width: 100%;
  }
}

@media (max-width: 500px) {
  .box_image {
    justify-content: space-around;
    flex-wrap: wrap;
  }

  .social {
    width: 34%;
    margin-bottom: 4%;
  }
}
</style>
