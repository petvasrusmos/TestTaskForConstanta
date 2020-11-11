<template>
  <div id="app">
    <side-bar></side-bar>
    <div>
      <Header/>
    </div>
    <div class="container">
        <keep-alive>
          <router-view/>
        </keep-alive>
    </div>
    <Footer/>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
import Header from './components/Header.vue'
import SideBar from './components/SideBar.vue'
import Footer from './components/Footer.vue'
// import { store, mutations } from './store'
export default Vue.extend({
  components: {
    Header,
    SideBar,
    Footer
  }
})
</script>
<style lang="scss">
.container {
  width: 70%;
  margin: 0px auto;
  padding: 0px 10px;
  transform: rotate(0deg);
  transition: transform 0.5s ease;
}

@media screen and (max-width: 1150px) {
  .container {
    width: 100%;
    padding: 0px;
    // transform: rotate(360deg);
  }
}

</style>
