<template>
  <div class="empresas-content">
    <div class="empresas-header">
      <h3>Empresas que já passaram por aqui:</h3>
    </div>
    <div class="empresas-slider">
      <div class="empresas-slider-container">
        <div class="swiper">
          <div class="empresas-slider-content">
            <div class="swiper-wrapper">
              <div class="swiper-slide">
                <div class="empresas-slider-logo parceiro-01"></div>
              </div>
              <div class="swiper-slide">
                <div class="empresas-slider-logo parceiro-02"></div>
              </div>
              <div class="swiper-slide">
                <div class="empresas-slider-logo parceiro-03"></div>
              </div>
            </div>
          </div>
        </div>

        <!-- If we need navigation buttons 
            <div class="swiper-button-prev slider-navbutton empresas-slider-button"></div>
            <div class="swiper-button-next slider-navbutton empresas-slider-button"></div>
            -->
        <!-- If we need pagination -->
        <div class="swiper-pagination"></div>

      </div>
    </div>
  </div>
</template>

<script>
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';

import Swiper, { Navigation, Pagination, Autoplay } from 'swiper';

export default {
  mounted() {
    this.swiper = new Swiper('.empresas-slider-content', {
      modules: [ Navigation, Pagination, Autoplay ],
      slidesPerView: 1,
      autoplay: {
        delay: 3000,
      },
      spaceBetween: 20,
      loop: true,
      grabCursor: true,
      pagination: {
        el: '.empresas-slider-container .swiper-pagination',
        clickable: true,
        dynamicBullets: true,
      },
      navigation: {
        nextEl: '.empresas-slider-container .swiper-button-next',
        prevEl: '.empresas-slider-container .swiper-button-prev',
      },
      breakpoints: {
        600: {
          slidesPerView: 2,
        },
        800: {
          slidesPerView: 3,
        }
      }
    });
  },
  destroyed() {
    this.swiper = null;
  },
  data() {
    return {
      swiper: null,
    };
  }
}
</script>

<style scoped>
.empresas-slider-container {
  position: relative;
}

.empresas-content {
  margin-top: 150px;
  display: flex;
  align-items: center;
}

.empresas-header {
  width: 30%;
  padding: 30px;
}

.empresas-header h3 {
  font-size: 26px;
  font-weight: 700;
  padding-left: 10px;
  border-left: 1px solid var(--primary-color);
}

.empresas-slider {
  width: 70%;
}

.empresas-slider-logo {
  width: 100%;
  height: 150px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
}

.parceiro-01 { background-image: url('../../../assets/img/parceiro-01.png'); }
.parceiro-02 { background-image: url('../../../assets/img/parceiro-02.png'); }
.parceiro-03 { background-image: url('../../../assets/img/parceiro-03.png'); }
.parceiro-04 { background-image: url('../../../assets/img/parceiro-04.png'); }
.parceiro-05 { background-image: url('../../../assets/img/parceiro-05.png'); }
.parceiro-06 { background-image: url('../../../assets/img/parceiro-06.png'); }

.swiper-horizontal>.swiper-pagination-bullets, .swiper-pagination-bullets.swiper-pagination-horizontal, .swiper-pagination-custom, .swiper-pagination-fraction {
  bottom: -10px;
}

@media screen and (max-width: 815px) {
  .empresas-content {
    flex-direction: column;
    align-items: flex-start;
  }

  .empresas-header {
    width: 100%;
  }

  .empresas-slider {
    width: 100%;
  }
}
</style>