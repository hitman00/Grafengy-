<template>
  <div :class="$style.slider_main">
    <div :class="$style.title">WHAT WE DO.</div>
    <div :class="$style.description">
      We help non-profits, govermental agencies, ethical businesses and research
      institutes speak directly to their audience with carefully crafted
      communication.
    </div>
    <div :class="$style.box">
      <div v-for="(i, id) in list" :key="id" :class="$style.cards">
        <div :class="$style.card_img"><img :src="i.img" /></div>
        <div :class="$style.card_title">{{ i.title }}</div>
        <div :class="$style.card_description">{{ i.description }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Slider',
  data: () => ({
    list: [
      {
        img: require('@/assets/imgs/slider1.png'),
        title: 'Branding',
        description:
          'Branding your startup or your company or project for elevate it.',
      },
      {
        img: require('@/assets/imgs/computer.png'),
        title: 'UI/UX Design',
        description:
          'Branding your startup or your company or project for elevate it.',
      },
      {
        img: require('@/assets/imgs/css.png'),
        title: 'Web Development',
        description:
          'Branding your startup or your company or project for elevate it.',
      },
      {
        img: require('@/assets/imgs/notepad.png'),
        title: 'APP DEVELOPMENT',
        description:
          'Branding your startup or your company or project for elevate it.',
      },
      {
        img: require('@/assets/imgs/protect.png'),
        title: 'Web Security',
        description:
          'Branding your startup or your company or project for elevate it.',
      },
      {
        img: require('@/assets/imgs/rocket.png'),
        title: 'Digital Markting',
        description:
          'Branding your startup or your company or project for elevate it.',
      },
    ],
  }),
}
</script>

<style lang="scss" module>
.slider_main {
  width: 100%;
}

.box {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  margin-top: 4%;
}

.cards {
  width: 30%;
  box-shadow: 1px 3px 6px #dddcdc;
  padding: 3%;
  margin-bottom: 3%;
  border-radius: 10px;
  transition: all 0.3s ease;
  cursor: pointer;
  &:hover {
    background: #399efc;
  }
}

.title {
  font-weight: 700;
  font-size: 50px;
  text-align: center;
  margin: 5.5% 0 2.1%;
}

.description {
  margin: 0 22%;
  text-align: center;
}

.card_img {
  position: relative;
  width: 26%;
  &:before {
    content: '';
    display: block;
    padding-bottom: 100%;
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

.card_title {
  font-weight: 600;
  font-size: 25px;
  margin: 3% 0;
}

.card_description {
}
</style>
