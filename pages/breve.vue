<template>
  <div class="container">
    <Head>
      <Title>Site em contrução</Title>
    </Head>

    <div class="container-overlay">
      <div class="container-row">
        <div class="logo-img">
          <img src="~/assets/img/engenharia-logo-clara.png" alt="Logo da empresa"/> 
        </div>

        <h2>Site em construção</h2>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Blanditiis temporibus, molestiae, quasi modi non explicabo iure suscipit provident autem a mollitia placeat quas at totam consequuntur, pariatur eum facilis animi.</p>

        <count-down />
        <social-icons />

        <NuxtLink to="/">Voltar</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
import '@/assets/css/reset.css'
import '@/assets/css/global.css'
import '@/assets/css/fontawesome.min.css'

import CountDown from '@/components/Breve/CountDown.vue'
import SocialIcons from '@/components/Breve/SocialIcons.vue'

export default {
  components: { CountDown, SocialIcons }
}
</script>

<style scoped>
.container {
  height: 100vh;
  background-image: url('~/assets/img/background-trator.jpg');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}

.container-overlay {
  height: 100%;
  padding: 20px;
  background-image: radial-gradient(rgba(3, 15, 39, 0.8), rgba(3, 15, 39, 0.95));
}

.container-row {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 35%;
  margin: 0 auto;
}

h2 {
  color: var(--white-color);
  text-transform: uppercase;
  text-align: center;
  font-weight: 900;
  font-size: 3.5rem;
  margin-top: 30px;
  margin-bottom: 20px;
}

p {
  color: var(--white-transp-color);
  text-align: center;
  width: 100%;
}

@media screen and (max-width: 2340px) {
  .container-row {
    width: 40%;
  }
}

@media screen and (max-width: 1750px) {
  .container-row {
    width: 50%;
  }
}

@media screen and (max-width: 1425px) {
  .container-row {
    width: 60%;
  }
}

@media screen and (max-width: 1215px) {
  .container-row {
    width: 70%;
  }
}

@media screen and (max-width: 1040px) {
  .container-row {
    width: 80%;
  }
}

@media screen and (max-width: 900px) {
  .container-row {
    width: 90%;
  }
}

@media screen and (max-width: 590px) {
  h2 {
    font-size: 2.1rem;
  }
}
</style>