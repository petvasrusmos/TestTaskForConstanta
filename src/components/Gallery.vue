<template>
 <div class="child-page-listing">
  <div class="grid-container">
    <div
      class="grid-container-list"
      v-for="(imageInfo, index) in galleryData"
      :key="index"
    >
      <div class="relative">
       <div class="grid-container-title">
         {{imageInfo.title}}
       </div>
       <img
         class="grid-container-img"
         :src="imageInfo.path"
         alt="gallery__photo"
       >
      </div>
    </div>
  </div>
 </div>
</template>
<script lang>
import Vue from 'vue'
export default Vue.extend({
  components: {
  },
  data () {
    return {
      galleryData: [
        {
          title: 'я злой',
          path: 'https://sun9-4.userapi.com/B_TTD1LGZwSgeAlREq4oPMlyoir2awElQKjDZw/jeWnPRVoB30.jpg'
        },
        {
          title: 'я добрый',
          path: 'https://sun9-54.userapi.com/Yl66Vn903RFVsQDUakT5AQTQYpgFrocICeT77Q/28l562HDZeM.jpg'
        },
        {
          title: 'я угрюмый',
          path: 'https://sun9-56.userapi.com/8sZ-dOs-Qsv3uPgKYgATRVSaSKhYfdvwslnC3Q/DJ2ms1Hru9A.jpg'
        }
      ]
    }
  }
})
</script>
<style lang="scss">
.relative {
  position: relative;
}
.grid-container-img {
  width: 100%;
  height: 550px;
  max-width: 300px;
  object-fit: cover;
  filter: blur(0px);
  transition: filter 0.3s ease-in;
}
.grid-container-img:hover {
  filter: blur(2px);
}
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  grid-gap: 3em;
}
.grid-container-list {
  position: relative;
  display: flex;
  justify-content: center;
  min-width: 200px;
}
.grid-container-title {
  text-transform: uppercase;
  letter-spacing: 1px;
  font-family: 'Lato', Arial, Helvetica, sans-serif;
  font-size: 1.5em;
  font-weight: bold;
  text-decoration: none;
  z-index: 1;
  position: absolute;
  width: 100%;
  max-width: 300px;
  height: 550px;
  top: 0;
  left: 0;
  opacity: 0;
  transition: opacity .5s;
  background: rgb(111, 100, 158, 0.6);
  color: white;
  /* position the text in t’ middle*/
  display: flex;
  align-items: center;
  justify-content: center;
  &:hover {
    opacity: 1;
  }
}

</style>
