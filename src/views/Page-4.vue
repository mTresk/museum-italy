<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <div class="screen__content">
            <div class="screen__images">
              <div style="width: 600px; height: 500px" class="screen__image screen__image-ibg">
                <img src="img/4.jpg" alt=""/>
              </div>
              <div class="screen__info screen__info_right">
                <h2 class="screen__subtitle screen__subtitle_h3">СЕРЬЁЗНЫЕ НЕДОСТАТКИ:</h2>
                <ul class="screen__text">
                  <li>тело слишком длинное;</li>
                  <li>наклонная постановка тела;</li>
                  <li>короткие ноги,</li>
                  <li>округлая голова, слишком плоская спереди;</li>
                  <li>слишком длинный, тонкий или очень короткий клюв, расположенный под прямым углом;</li>
                  <li>шея слишком короткая, отсутствуют оборки на груди;</li>
                  <li>несоответствие в окраске.</li>
                </ul>
                <h2 class="screen__subtitle screen__subtitle_h3">ПОРЯДОК ОЦЕНКИ:</h2>
                <ul class="screen__text">
                  <li>форма головы и клюва, длина шеи, туловища и ног; цвет оперения, глаз и клюва; общее
                    впечатление.
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <Navigation :page-next="pageNext" :page-prev="pagePrev"/>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import {mapActions} from 'vuex'
import Navigation from "@/components/Navigation";
import Doves from "@/components/Doves";
import Logo from "@/components/Logo";
import Background from "@/components/Background";

export default {
  name: "Page-4",
  data() {
    return {
      pagePrev: 'page-3',
      pageNext: 'home',
    }
  },
  components: {
    Doves,
    Logo,
    Background,
    Navigation
  },
  mounted() {
    this.animate()
  },
  methods: {
    ...mapActions([
      'animate'
    ]),
  }
}
</script>