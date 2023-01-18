<template>
  <div class="banner-container" :style="styleContainer">
    <div class="banner-overlay">
      <div class="banner-content">
        <h1>Tiramos o seu projeto dos sonhos do papel</h1>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Neque quibusdam aliquam eos? Maiores ut exercitationem nisi impedit officia, voluptates, quisquam adipisci.</p>
        <NuxtLink to="/breve/">Peça o seu orçamento</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
import imgSlideContrucao01 from '../../assets/img/construcao-01.jpg'
import imgSlideProjeto01 from '../../assets/img/projeto-01.jpg'
import imgSlideProjeto02 from '../../assets/img/projeto-02.jpg'

export default {
  mounted() {
    setInterval(() => { this.play(); }, 5000);
  },
  data() {
    return {
      index: 0,
      images: [
        imgSlideContrucao01, 
        imgSlideProjeto01, 
        imgSlideProjeto02
      ]
    };
  },
  methods: {
    play() {
      this.index++;
    }
  },
  computed: {
    styleContainer() {
      if (this.index >= this.images.length) {
        this.index = 0;
      }

      let image = this.images[ this.index ];
      return `background-image: url('${image}');`;
    }
  }
}
</script>

<style scoped>
.banner-container {
  margin: 0;
  padding: 0;
  transition: background-image 2s ease-in-out;
  background-size: cover;
}

.banner-overlay {
  background-color: var(--accent-overlay80);
  height: 100%;
  width: 100%;
  padding-bottom: 50px;
}

.banner-content {
  width: var(--default-content-width);
  margin: 0 auto;
  height: 650px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  opacity: 1;
}

.banner-content h1 {
  color: var(--white-color);
  font-weight: 900;
  font-size:3.2rem;
  text-transform: uppercase;
  text-align: center;
  line-height: 1.2;
  margin-top: -100px;
}

.banner-content p {
  color: var(--white-transp-color);
  text-align: center;
  font-size: 1.2rem;
  line-height: 1.2;
  padding: 15px 0;
  width: 80%;
}

.banner-content a {
  text-decoration: none;
  line-height: 1.2em;
  font-size: 1.2rem;
  font-weight: 900;
  text-transform: uppercase;
  background-color: var(--primary-color);
  padding: 15px 30px;
  opacity: 1;
  margin-top: 20px;
}

@media screen and (max-width: 840px) {
  .banner-content h1 {
    font-size: 2.5rem;
  }
}
</style>