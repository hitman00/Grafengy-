<template>
  <div :class="$style.header_main">
    <div :class="$style.logo">
      <div :class="$style.logo_img"><img src="@/assets/imgs/logo4.png" /></div>
      Grafengy
    </div>
    <div :class="$style.meno">
      <img src="@/assets/imgs/menobar.png" />
      <ul>
        <li>Home</li>
        <li>About</li>
        <li>Services</li>
        <li>Projects</li>
        <li>Contact Us</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="scss" module>
.header_main {
  width: 100%;
  display: flex;
  padding: 2% 0;
}

.logo {
  width: 25%;
  display: flex;
  align-items: center;
  font-weight: 700;
  font-size: 30px;
}

.logo_img {
  position: relative;
  margin-right: 5%;
  width: 24%;
  &:before {
    content: '';
    display: block;
    padding-bottom: 87%;
  }
  img {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    width: 100%;
  }
}

.meno {
  width: 75%;
  ul {
    display: flex;
    justify-content: end;
    align-items: center;
    cursor: pointer;
    li {
      padding: 1.5% 3%;
      color: #afafaf;
      transition: all 0.3s ease;
      border-radius: 10px;
      font-weight: 500;
      &:hover {
        background: #399efc;
        color: #fff;
      }
    }
  }
  img {
    display: none;
    width: 25px;
    float: right;
    margin-top: 4%;
    margin-right: 3%;
  }
}

@media (max-width: 800px) {
  .meno {
    width: 50%;
    ul {
      display: none;
    }
    img {
      display: block;
    }
  }

  .logo {
    width: 50%;
  }

  .logo_img {
    margin-right: 3%;
    width: 15%;
  }
}

@media (max-width: 500px) {
  .logo {
    font-size: 20px;
  }
}
</style>
