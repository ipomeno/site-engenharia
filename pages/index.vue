<template>
  <Head>
    <Title>Bem vindo ao site</Title>
  </Head>
  <header-top />
  <header-nav-bar />
  <home-banner />
  <home-categorias />
  <home-sobre />
  <home-servicos />
  <home-citacoes />
  <home-solicite-orcamento />
  <page-footer />
</template>

<script>
import '@/assets/css/reset.css'
import '@/assets/css/global.css'
import '@/assets/css/fontawesome.min.css'

import HeaderTop from '~~/components/HeaderTop.vue'
import HeaderNavBar from '~~/components/HeaderNavBar.vue'
import PageFooter from '~~/components/PageFooter.vue'
import HomeBanner from '~~/components/Home/HomeBanner.vue'
import HomeCategorias from '~~/components/Home/HomeCategorias.vue'
import HomeSobre from '~~/components/Home/HomeSobre.vue'
import HomeServicos from '~~/components/Home/HomeServicos.vue'
import HomeCitacoes from '~~/components/Home/HomeCitacoes.vue'
import HomeSoliciteOrcamento from '~~/components/Home/HomeSoliciteOrcamento.vue'

export default {
  components: {
    HeaderNavBar,
    HeaderTop,
    PageFooter,
    HomeBanner,
    HomeCategorias,
    HomeSobre,
    HomeServicos,
    HomeCitacoes,
    HomeSoliciteOrcamento,
  }
}
</script>