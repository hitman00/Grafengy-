<template>
  <div :class="$style.footer_main">
    <div :class="$style.footer_box">
      <div :class="$style.about_box">
        <div :class="$style.title">About Us</div>
        <div :class="$style.line"><span></span></div>
        <div :class="$style.description">
          We help non-profits, govermental agencies, ethical businesses and
          research institutes speak directly to their audience with carefully
          crafted communication
        </div>
        <div :class="$style.social">
          <span v-for="img in images" :key="img.id">
            <img :src="img" />
          </span>
        </div>
      </div>
      <div :class="$style.link_box">
        <div v-for="(i, id) in list" :key="id" :class="$style.link_slide">
          <div :class="$style.title">{{ i.title }}</div>
          <div :class="$style.line"><span></span></div>
          <div
            v-for="item in i.page"
            :key="item.id"
            :class="$style.description"
          >
            {{ item }}
          </div>
        </div>
      </div>
    </div>
    <div :class="$style.copy_right">Copyright By @Mohammad Rezaee - 2021</div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data: () => ({
    list: [
      {
        title: 'Our Links',
        page: ['Home', 'About Us', 'Services', 'Team', 'Blog'],
      },
      {
        title: 'Our Services ',
        page: [
          'Strategy & Research',
          'Web Development',
          'Web Solution ',
          'Digital Marketing',
          'App Design',
        ],
      },
      {
        title: 'Other Links',
        page: [
          'FAQ',
          'Portfolio',
          'Privacy Policy',
          'Term & Conditions',
          'Support',
        ],
      },
    ],
    images: [
      require('@/assets/imgs/facebook_logo2.png'),
      require('@/assets/imgs/instagran_logo2.png'),
      require('@/assets/imgs/twitter_logo2.png'),
    ],
  }),
}
</script>

<style lang="scss" module>
.footer_main {
  background: #2d2d2d;
}

.footer_box {
  display: flex;
  max-width: 1200px;
  margin: 0 auto;
  color: #fff;
  padding: 5% 15px;
}

.about_box {
  width: 30%;
}

.link_box {
  width: 70%;
  display: flex;
  justify-content: space-evenly;
}

.title {
  font-weight: 600;
  font-size: 25px;
}

.link_slide {
  width: 30%;
}

.social {
  display: flex;
  margin-right: 20%;
  span {
    width: 20%;
    display: block;
    background: #399efc;
    border-radius: 50%;
    margin-right: 4%;
    transition: all 0.4s ease;
    cursor: pointer;
    img {
      display: block;
      width: 100%;
      margin: 0 auto;
      padding: 20%;
    }
    &:hover {
      background: #f938bf;
    }
  }
}

.line {
  width: 20px;
  height: 4px;
  border-radius: 50px;
  background: #fff;
  margin: 5% 0;
  span {
    margin-left: 26px;
    width: 50px;
    height: 4px;
    background: #fff;
    border-radius: 50px;
    display: block;
  }
}

.description {
  font-weight: 300;
  margin: 9% 11% 9% 0%;
}

.copy_right {
  border-top: 1px solid #ffffff61;
  font-weight: 300;
  text-align: center;
  color: #ffffffd6;
  max-width: 1200px;
  margin: 0 auto;
  padding: 1% 0;
  font-size: 18px;
}
</style>
