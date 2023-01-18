<template>
  <div class="slider-container">
    <div class="swiper">
      <div class="slider-content">
        <div class="swiper-wrapper">

          <div class="swiper-slide">
            <div class="citacoes-item">
              <div class="citacoes-item-text">
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aliquid ea, fuga excepturi doloremque sed
                  molestias eligendi necessitatibus vel ad quidem natus, sequi repellendus obcaecati eaque at quia! In,
                  ad magnam.</p>
              </div>
              <div class="citacoes-item-caption">
                <div class="citacoes-item-caption-image citacoes-person-01"></div>
                <div class="citacoes-item-caption-person">
                  <div class="citacoes-item-caption-name">John Doe</div>
                  <div class="citacoes-item-caption-cargo">CEO</div>
                </div>
              </div>
            </div>
          </div>

          <div class="swiper-slide">
            <div class="citacoes-item">
              <div class="citacoes-item-text">
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aliquid ea, fuga excepturi doloremque sed
                  molestias eligendi necessitatibus vel ad quidem natus, sequi repellendus obcaecati eaque at quia! In,
                  ad magnam.</p>
              </div>
              <div class="citacoes-item-caption">
                <div class="citacoes-item-caption-image citacoes-person-02"></div>
                <div class="citacoes-item-caption-person">
                  <div class="citacoes-item-caption-name">John Doe</div>
                  <div class="citacoes-item-caption-cargo">CEO</div>
                </div>
              </div>
            </div>
          </div>

          <div class="swiper-slide">
            <div class="citacoes-item">
              <div class="citacoes-item-text">
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aliquid ea, fuga excepturi doloremque sed
                  molestias eligendi necessitatibus vel ad quidem natus, sequi repellendus obcaecati eaque at quia! In,
                  ad magnam.</p>
              </div>
              <div class="citacoes-item-caption">
                <div class="citacoes-item-caption-image citacoes-person-03"></div>
                <div class="citacoes-item-caption-person">
                  <div class="citacoes-item-caption-name">John Doe</div>
                  <div class="citacoes-item-caption-cargo">CEO</div>
                </div>
              </div>
            </div>
          </div>

          <div class="swiper-slide">
            <div class="citacoes-item">
              <div class="citacoes-item-text">
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aliquid ea, fuga excepturi doloremque sed
                  molestias eligendi necessitatibus vel ad quidem natus, sequi repellendus obcaecati eaque at quia! In,
                  ad magnam.</p>
              </div>
              <div class="citacoes-item-caption">
                <div class="citacoes-item-caption-image citacoes-person-04"></div>
                <div class="citacoes-item-caption-person">
                  <div class="citacoes-item-caption-name">John Doe</div>
                  <div class="citacoes-item-caption-cargo">CEO</div>
                </div>
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>

    <!-- If we need navigation buttons -->
    <div class="swiper-button-prev slider-navbutton"></div>
    <div class="swiper-button-next slider-navbutton"></div>
    <!-- If we need pagination -->
    <div class="swiper-pagination"></div>
  </div>
</template>

<script>
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';

import Swiper, { Navigation, Pagination } from 'swiper'
export default {
  mounted() {
    this.swiper = new Swiper('.slider-content', {
      modules: [ Navigation, Pagination ],
      spaceBetween: 20,
      slidesPerView: 1,
      loop: true,
      grabCursor: true,
      pagination: {
        el: '.slider-container .swiper-pagination',
        clickable: true,
        dynamicBullets: true,
      },
      navigation: {
        nextEl: '.slider-container .swiper-button-next',
        prevEl: '.slider-container .swiper-button-prev'
      },
      breakpoints: {
        790: {
          slidesPerView: 2,
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
  },
}
</script>

<style scoped>
.slider-container {
  position: relative;
  padding: 0px 60px;
}

.citacoes-item {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
}

.citacoes-item-caption {
  margin-top: 20px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
}

.citacoes-item-caption-image {
  width: 50px;
  height: 50px;
  border-radius: 25px;
  border: 3px solid var(--white-transp-color);
  margin-right: 10px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

.swiper-horizontal>.swiper-pagination-bullets, .swiper-pagination-bullets.swiper-pagination-horizontal, .swiper-pagination-custom, .swiper-pagination-fraction {
  bottom: -30px;
}

.swiper-button-prev {
  left: 10px;
}

.swiper-button-next {
  right: 10px;
}

.citacoes-person-01 { background-image: url('../../../assets/img/citacao-person-01.jpg'); }
.citacoes-person-02 { background-image: url('../../../assets/img/citacao-person-02.jpg'); }
.citacoes-person-03 { background-image: url('../../../assets/img/citacao-person-03.jpg'); }
.citacoes-person-04 { background-image: url('../../../assets/img/citacao-person-04.jpg'); }

</style>