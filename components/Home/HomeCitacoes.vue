<template>
  <div class="citacoes-container">
    <div class="citacoes-content">
      <div class="citacoes-header">
        <p>O que estão</p>
        <h2>Dizendo sobre nós</h2>
      </div>

      <home-citacoes-depoimentos />
      <home-citacoes-empresas />
    </div>
  </div>
</template>

<script>
import HomeCitacoesDepoimentos from '~/components/Home/Citacoes/HomeCitacoesDepoimentos.vue'
import HomeCitacoesEmpresas from '~/components/Home/Citacoes/HomeCitacoesEmpresas.vue';

export default {
  components: { 
    HomeCitacoesDepoimentos,
    HomeCitacoesEmpresas,
  },
}
</script>

<style scoped>
.citacoes-container {
  background-image: url('../../assets/img/background-depoimentos.jpg');
  color: var(--white-color);
  background-position: top left;
  background-repeat: no-repeat;
  background-size: cover;
}

.citacoes-content {
  width: var(--default-content-width);
  margin: 0 auto;
  padding: 50px 0px 100px 0px;
}

.citacoes-header {
  padding: 30px;
}

.citacoes-header p {
  color: var(--primary-color);
  font-weight: 400;
  letter-spacing: 1px;
  text-transform: uppercase;
  height: 21px;
}

.citacoes-header h2 {
  padding: 0px 0px 0px 15px;
  margin: 10px 0px;
  color: var(--white-color);
  font-weight: 700;
  font-size: 4rem;
  border-left: 2px solid var(--primary-color);
}

@media screen and (max-width: 280px) {
  .citacoes-header h2 {
    font-size: 2.6rem;
  }
}
</style>