<template>
  <div class="servicos-container">
    <div class="servicos-content">

      <div class="servicos-item servicos-header-align">
        <div class="servicos-header">
          <p>Conheça os</p>
          <h2>Nossos serviços</h2>
          <div class="servicos-buttons"> <a href="javascript:void(0);" class="btn-saiba-mais">Saiba mais</a> </div>
        </div>
      </div>
      <div class="servicos-item">
        <div class="card-servico card-pavimento">
          <div class="card-servico-content">
            <h2>Pavimentação</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit provident repellat quod.</p>
            <div class="card-buttons">
              <a href="javascript:void(0)" class="btn-saiba-mais">Saiba mais</a>
            </div>
          </div>
        </div>
      </div>

      <div class="servicos-item">
        <div class="card-servico card-laudo">
          <div class="card-servico-content">
            <h2>Laudo técnico</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit provident repellat quod.</p>
            <div class="card-buttons">
              <a href="javascript:void(0)" class="btn-saiba-mais">Saiba mais</a>
            </div>
          </div>
        </div>
      </div>

      <div class="servicos-item">
        <div class="card-servico card-infra">
          <div class="card-servico-content">
            <h2>Infraestrutura</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit provident repellat quod.</p>
            <div class="card-buttons">
              <a href="javascript:void(0)" class="btn-saiba-mais">Saiba mais</a>
            </div>
          </div>
        </div>
      </div>

      <div class="servicos-item">
        <div class="card-servico card-fundacao">
          <div class="card-servico-content">
            <h2>Fundações</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit provident repellat quod.</p>
            <div class="card-buttons">
              <a href="javascript:void(0)" class="btn-saiba-mais">Saiba mais</a>
            </div>
          </div>
        </div>
      </div>

      <div class="servicos-item">
        <div class="card-servico card-construcao">
          <div class="card-servico-content">
            <h2>Construção</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit provident repellat quod.</p>
            <div class="card-buttons">
              <a href="javascript:void(0)" class="btn-saiba-mais">Saiba mais</a>
            </div>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<style scoped>
.servicos-container {
  margin: 0 auto;
  width: var(--default-content-width);
  padding: 100px 0;
}

.servicos-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
}

.servicos-item {
  flex-grow: 1;
  width: 30%;
  height: 350px;
  margin: 5px;
}

.servicos-header-align {
  display: flex;
  align-items: flex-start;
  justify-content: center;
  flex-direction: column;
}

.servicos-header p {
  color: var(--primary-color);
  font-weight: 400;
  letter-spacing: 1px;
  text-transform: uppercase;
  height: 21px;
}

.servicos-header h2 {
  padding: 0px 0px 0px 15px;
  margin: 10px 0px;
  color: var(--accent-color);
  font-weight: 700;
  font-size: 4rem;
  border-left: 2px solid var(--primary-color);
}

.servicos-buttons {
  margin-top: 40px;
}

.card-servico {
  background-size: 100% 100%;
  background-position: center;
  background-repeat: no-repeat;
  height: 100%;

  display: flex;
  align-items: flex-end;
  justify-content: flex-start;
}

/*
.card-servico-content {
  transform: scale(0.9);
}
*/

.card-servico:hover {
  background-size: 130% auto;
}

/*
.card-servico:hover .card-servico-content {
  transform: scale(1);
}
*/

.card-pavimento {
  background-image: url('../../assets/img/pavimentacao.png');
}

.card-laudo {
  background-image: url('../../assets/img/laudotecnico.png');
}

.card-infra {
  background-image: url('../../assets/img/infraestrutura.png');
}

.card-fundacao {
  background-image: url('../../assets/img/fundacao.png');
}

.card-construcao {
  background-image: url('../../assets/img/construcao.png');
}

.card-servico-content {
  padding: 20px;
}

.card-servico-content h2 {
  font-weight: 700;
  padding-bottom: 10px;
  font-size: 1.2rem;
  color: var(--primary-color);
}

.card-servico-content p {
  line-height: 1.4rem;
  font-weight: 400;
  padding-bottom: 10px;
  font-size: 0.9rem;
  color: var(--white-transp-color);
}

.card-buttons {
  margin: 20px 0px;
}

@media screen and (max-width: 1240px) {
  .servicos-item {
    width: 40%;
  }
}

@media screen and (max-width: 840px) {
  .servicos-item {
    width: 90%;
  }
}

@media screen and (max-width: 280px) {
  .servicos-header h2 {
    font-size: 2.6rem;
  }
  
}
</style>