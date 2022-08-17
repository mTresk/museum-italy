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
              <div style="width: 485px; height: 500px" class="screen__image screen__image-ibg">
                <img src="img/3.jpg" alt=""/>
              </div>
              <div class="screen__info screen__info_right">
                <p class="screen__text">
                  ШЕЯ: Средней длины, слегка изогнута назад, гордо поставлена, более тонкая в средней части,
                  расширяется к груди. На шее есть бант,
                  который заканчивается на груди.
                </p>
                <p class="screen__text">ГРУДЬ: Широкая и округлая.</p>
                <p class="screen__text">СПИНА: Широкая, плоская, горизонтальная.</p>
                <p class="screen__text">КРЫЛЬЯ: Не слишком длинные, лежат на хвосте, неплотно прилегают к
                  туловищу.</p>
                <p class="screen__text">ХВОСТ: Немного короче среднего, горизонтально расположен, закрыт.</p>
                <p class="screen__text">НОГИ: Свободные от перьев, средней длины. Цевка полностью видна, птица стоит
                  на кончиках пальцев.</p>
                <p class="screen__text">
                  ЦВЕТ: белый, чёрный, сероватый, красный, жёлтый, серебряный, серебристо-бурый, пепельный,
                  пепельно-красный, кремовый.
                </p>
                <p class="screen__text">ЦВЕТА И МЕТКИ: все цвета; окрас насыщенный, равномерно распределён по всему
                  телу.</p>
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
  name: "Page-3",
  data() {
    return {
      pagePrev: 'page-2',
      pageNext: 'page-4',
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