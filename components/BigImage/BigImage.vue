<template>
  <div :class="$style.image_main">
    <div :class="$style.bg_img">
      <img src="@/assets/imgs/background1.png" />
    </div>
    <div :class="$style.box">
      <div :class="$style.title">Let's start Something big Together.</div>
      <div :class="$style.description">
        We are a full service design agency that drives positive change around
        social, economic, and environmental issues Through creative
        communication and strategy, we build experiences that inspire dialogue
        and action.
      </div>
      <div :class="$style.btn">Know More</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BigImage',
}
</script>

<style lang="scss" module>
.image_main {
  position: relative;
}

.bg_img {
  position: relative;
  width: 100%;
  &:before {
    content: '';
    display: block;
    padding: 25.1%;
  }
  img {
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    width: 100%;
    border-radius: 30px;
  }
}

.box {
  position: absolute;
  width: 50%;
  top: 10%;
  color: #fff;
  left: 5%;
}

.title {
  font-weight: 700;
  font-size: 50px;
  line-height: 1.2;
}

.description {
  font-size: 20px;
  margin: 3% 0 6%;
}

.btn {
  background: #399efc;
  padding: 2% 6%;
  display: inline-block;
  border-radius: 5px;
  transition: all 0.3s ease;
  cursor: pointer;
  font-weight: 600;
  &:hover {
    opacity: 0.8;
  }
}
</style>
