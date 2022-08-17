<template>
  <main class="page">
    <div class="screen">
      <Background/>
      <div class="screen__container">
        <Logo/>
        <div class="screen__body">
          <Doves/>
          <h2 class="screen__subtitle">ВНЕШНИЙ ВИД</h2>
          <div class="screen__content">
            <div class="screen__images">
              <div style="width: 485px; height: 500px" class="screen__image screen__image-ibg">
                <img src="img/2.jpg" alt=""/>
              </div>
              <div class="screen__info screen__info_right">
                <p class="screen__text">Итальянская чайка - изящный, небольшой (30-32 см в длину) голубь на высоких
                  ногах.</p>
                <p class="screen__text">
                  ГОЛОВА: Маленькая и широкая. Верх головы уплощённый, но передняя и задняя части подходят кверху под
                  тупым углом. Перед клювом среднего
                  размера возвышение.
                </p>
                <p class="screen__text">ГЛАЗА: Большие, яркие, оранжевого цвета. Белые и пёстрые имеют темные
                  глаза.</p>
                <p class="screen__text">Цвет века соответствует цвету оперения. Ледяные имеют цвет века от
                  сливово-голубого до серо-голубого.</p>
                <p class="screen__text">
                  КЛЮВ: Средней длины, слегка опущенный вниз под тупым углом. Цвет соответствует цвету оперения.
                  Ледяные имеют чёрный клюв. Серёжка
                  маленькая тонкой текстуры, не очень развита.
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
  name: "Page-2",
  data() {
    return {
      pagePrev: 'page-1',
      pageNext: 'page-3',
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