<template>
  <div class="header-wrapper">
    <div class="header-wrapper__top">
      <div class="container">
        <div class="header">
          <div class="header__logo">
            <img
              class="header__img"
              alt="Vue logo"
              src="../assets/doggy.png">
            <div class="header__title">
              Like Milk
            </div>
          </div>
          <Burger />
        </div>
      </div>
    </div>
    <div class="header-wrapper__nav">
      <div class="container">
        <div class="header">
          <router-link class="header__button" to="/"><span>About me</span></router-link>
          <router-link class="header__button" to="/map"><span>Map</span></router-link>
          <router-link class="header__button" to="/gallery"><span>Gallery</span></router-link>
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
import Burger from './Burger.vue'
export default Vue.extend({
  components: {
    Burger
  }
})
</script>
<style lang="scss">

$header-height: 90px;
$text-color: #000000bd;

.header-wrapper {
  -webkit-box-shadow: 0px 13px 29px -9px rgba(0,0,0,0.09);
  -moz-box-shadow: 0px 13px 29px -9px rgba(0,0,0,0.09);
  box-shadow: 0px 13px 29px -9px rgba(0,0,0,0.09);
  margin-bottom: 60px;

  &__top {
    display: flex;
    background: rgb(111, 100, 158);
  }
  &__nav {
    width: 100%;
    height: ($header-height * 0.6);
    display: flex;
  }
}
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100%;
  &__logo {
    display: flex;
    align-items: center;
  }
  &__title {
    display: block;
    padding-left: 16px;
    font-size: 38px;
    text-transform: uppercase;
    letter-spacing: 1px;
    width: 10px;
    height: 100%;
    color: rgb(255, 255, 255);
    font-family: 'Lato', Arial, Helvetica, sans-serif;
  }
  &__img {
    height: 83px;
    filter: invert(100%);
    // transform: scale(-1, 1);
  }
  &__button {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #ffffff;
    position: relative;
    background: #ffffff;
    text-align: center;
    cursor: pointer;
    transition: all 0.1s ease-in-out;
    text-decoration: none;
    color: rgba(0, 0, 0, 0.842);
    span {
      font-family: 'Lato', Arial, Helvetica, sans-serif;
      font-size: 20px;
      text-transform: uppercase;

    }
    color: $text-color;
  }
}
.header__button:hover {
  opacity: 0.3;
  box-shadow: 6px 6px 10px rgba(0, 0, 0, 0.2);
}
.header__button:active {
  opacity: 1;
  box-shadow: inset 8px 8px 16px rgba(0, 0, 0, 0.1);
  color: $text-color;
}

@media screen and (max-width: 768px) {
  .header-wrapper {
    &__nav {
    display: none;
    }
  }

  .header__img {
    height: 47px;
  }
  .header__title {
    font-size: 23px;
  }
  .header-wrapper {
    margin-bottom: 20px;
  }
}
</style>
