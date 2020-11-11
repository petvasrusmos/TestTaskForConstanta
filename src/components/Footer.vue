<template>
    <div class="footer">
      <div class="footer__wrapper container">
        <div class="footet__info">
          <div class="footer__info-group group">
            <h3 class="group__title">Социальные сети</h3>
            <ul class="group__list">
              <li><a target="_blank" href="https://vk.com/id27263359" class="link footer__text">Вконтакте</a></li>
              <li><a target="_blank" href="https://www.instagram.com/petyashevlokov/" class="link footer__text">Instagram</a></li>
              <li><a target="_blank" href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" class="link footer__text">Одноклассники</a></li>
            </ul>
          </div>
        </div>
        <div class="footet__info">
          <div class="footer__info-group group">
            <h3 class="group__title">Контакты</h3>
            <ul class="group__list">
              <li><span class="footer__text">Петр </span></li>
              <li><span class="footer__text">Шевлоков </span></li>
              <li><span style="cursor: text" class="footer__text">+79777564391</span></li>
            </ul>
          </div>
        </div>
        <div class="footet__info">
          <div class="footer__info-group group">
            <h3 class="group__title">Сегодня</h3>
            <ul class="group__list group__list-middle">
              <li><span class="footer__text">дата: {{localDate}}</span></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
</template>
<script lang>
import Vue from 'vue'
export default Vue.extend({
  data () {
    return {
      date: 1580558031264
    }
  },
  mounted () {
    this.date = Date.now()
  },
  computed: {
    localDate: function () {
      return (new Date(this.date)).toLocaleDateString()
    }
  }
})
</script>
<style lang="scss" scoped>
.footer {
  display: flex;
  background: rgb(111, 100, 158);
  margin-top: 100px;
  flex: 0 0 auto;
  min-height: 200px;
  &__wrapper {
    display: flex;
    padding: 30px 5px;
    // padding-bottom: 20px;
    // padding-top: 20px;
    justify-content: space-around;
    color: white;
    flex-wrap: wrap;
    // border: 1px solid white;
  }
  &__info {
    margin: 5px 20px;
    border: 1px solid black;
  }
  &__info-group {
    display: flex;
    align-items: space-between;
    height: 90%;

  }
}
.group {
  flex-direction: column;
  padding: 5px 24px;
  max-width: 150px;
  &__title {
    cursor: default;
    margin-top: 0px;
    margin-bottom: 20px;
    letter-spacing: 1px;
    text-transform: uppercase;
    color: rgba(255, 255, 255, 0.753);
    font-size: 12px;
    font-weight: 600;
    line-height: 16px
  }
  &__list {
    text-align: start;
    display: flex;
    flex-flow: column wrap;
    height: 100%;
    justify-content: space-between;
    margin: 0;
    padding: 0;
    list-style: none;
    font-size: 14px;
    line-height: 16px;
    text-align: start;
  }
}

.group:last-child {
  justify-content: space-around;
  text-align: start;
}

.footer__text {
  font-family: 'Lato', Arial, Helvetica, sans-serif;
  text-decoration: none;
  color: rgba(255, 249, 249, 0.562);
  cursor: default;
}
.link {
  cursor: pointer;
  transition: color .15s ease-out;
}

.link:hover {
  color:rgb(255, 255, 255);
}

@media screen and (max-width: 768px) {
  .footer {
    margin-top: 20px;
  }
  .footer__wrapper {
    justify-content: start;
  }
  .group__title {
    margin-top: 20px;
  }
}
</style>
