<template>
  <div class="home">
    <div class="home__title fadeInLeft"> Приветствую</div>
    <div class="home__body fadeInRight">
      <p>
        <!-- Я должен, что-то про себя рассказать? Серьезно? НЕЕЕЕЕЕ. Давайте я лучше расскажу почему я назвал этот сайт LIKE MILK. -->
        Меня зовут Петр, мне 22, и я сверстал все, что вы видите вокруг этого, безусловно, очень интересного текста. Если вам вдруг захотелось узнать как выглядит этот гений, можете
        перейти в раздел GALLERY и посмотреть на три версии меня, что заперты в суровой, но от того не менее адаптивной, GRID сетке.</p>
        <p>
        Если вы вдруг захотите меня выследить и убить, то точный адрес я вам не скажу, это было бы слишком просто. Дам лишь маленькую подсказку. В разделе MAP есть GOOGLE карта, что меткой указывает на ближайшую ко мне станцию метро.
        Надеюсь, это вам не поможет.
        </p>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'Home',
  components: {
  }
})
</script>
<style lang="scss">
.home {
  display: flex;
  flex-direction: column;
  font-family: 'Lato', Arial, Helvetica, sans-serif;
  font-size: 25px;
  min-width: 320px;
  letter-spacing: 1px;
  color: #000000bd;
  &__body {
    width: 100%;
    padding: 20
  }
  &__title {
    text-align: center;
    font-weight: 300;
    letter-spacing: 2px;
    font-size: 30px;
    margin-bottom: 20px;
  }
}

.fadeInLeft {
  animation-name: fadeInLeft;
  animation-duration: 1s;
  animation-fill-mode: both;
  animation-delay: 0.5s;
}
  @keyframes fadeInLeft {
  0% {
  opacity: 0;
  transform: translate3d(-35%, 0, 0);
  }
  100% {
  opacity: 1;
  transform: none;
  }
}
.fadeInRight {
  animation-name: fadeInRight;
  animation-duration: 1s;
  animation-fill-mode: both;
  animation-delay: 0.5s;
}
  @keyframes fadeInRight {
  0% {
  opacity: 0;
  transform: translate3d(35%, 0, 0);
  }
  100% {
  opacity: 1;
  transform: none;
  }
}
</style>
