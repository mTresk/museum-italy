<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <h2 class="screen__subtitle">Итальянская чайка</h2>
          <div class="screen__content">
            <div class="screen__images">
              <div style="width: 485px; height: 500px" class="screen__image screen__image-ibg">
                <img src="img/1.jpg" alt=""/>
              </div>
              <div class="screen__info screen__info_right">
                <p class="screen__text">Старинная порода из Верхней Италии (город Реджо-Эмилия). Итальянское
                  наименование - «Реггианино».</p>
                <p class="screen__text">
                  Итальянские чайки появились в начале XVIII века - видимо, в результате скрещивания чаек с моденским
                  куриным голубем. Разводились эти
                  птицы преимущественно в спортивных целях.
                </p>
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
import Background from "@/components/Background";
import Logo from "@/components/Logo";
import Doves from "@/components/Doves";

export default {
  name: "Page-1",
  data() {
    return {
      pageNext: 'page-2',
      pagePrev: 'home'
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