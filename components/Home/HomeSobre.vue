<template>
  <div class="sobre-container">
    <div class="sobre-content">
      <!-- <div class="sobre-image"></div> -->
      <img id="resumo-sobre" src="../../assets/img/resumo-sobre.jpg"/>
      <div class="sobre-pane">
        <p class="sobre-texto-inicio">Um pouco</p>
        <h2 class="sobre-titulo">Sobre a empresa</h2>
        <div class="sobre-texto">
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta maxime rem amet dolorem quas expedita nihil,
            id est quos excepturi aspernatur maiores nesciunt eum neque delectus ipsum facilis repudiandae libero.</p>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur voluptates reiciendis perspiciatis
            fugiat porro aliquam architecto eum dolor, harum, impedit voluptate corporis quaerat placeat autem.</p>
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Provident repellat quod molestiae sit! Quibusdam
            a nesciunt illo impedit neque ea, maiores repellat dolores harum repellendus aliquid, tempora at soluta
            molestias.</p>
          <div class="sobre-buttons"> <a href="javascript:void(0);" class="btn-saiba-mais">Saiba mais</a> </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.sobre-container {
  background-color: var(--white-cold-color);
  background-image: url('../../assets/img/background-sobre.jpg');
}

.sobre-content {
  margin: 0 auto;
  width: var(--default-content-width);
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  padding: 50px 0px;
}

/* .sobre-content .sobre-image {
  height: 500px;
  width: 100%;
  margin-right: -5%;
  background-color: #000;
  background-image: url('./img/resumo-sobre.jpg');
  background-position: top left;
  background-size: cover;
} */

.sobre-content #resumo-sobre {
  width: 500px;
  margin-right: -10%;
}

.sobre-content .sobre-pane {
  border: 1px solid rgba(0, 0, 0, 0.2);
  box-shadow: 0px 10px 35px rgba(0, 0, 0, 0.3);
  padding: 50px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  border-top: 3px solid var(--primary-color);
  background-color: var(--white-color);
}

.sobre-texto-inicio {
  color: var(--primary-color);
  font-weight: 400;
  letter-spacing: 1px;
  text-transform: uppercase;
  height: 21px;
}

.sobre-titulo {
  color: var(--accent-color);
  font-weight: 700;
  font-size: 3.6rem;
  padding-left: 15px;
  border-left: 2px solid var(--primary-color);
  margin: 10px 0px;
}

.sobre-texto {
  padding-top: 20px;
}

.sobre-texto p {
  color: #666;
  font-weight: 400;
  padding-top: 10px;
}

.sobre-texto .sobre-buttons {
  margin-top: 30px;
}

.sobre-texto a.btn-saiba-mais {
  text-decoration: none;
  font-size: 0.9rem;
  letter-spacing: 1px;
  font-weight: 600;
  text-transform: uppercase;
  background-color: var(--primary-color);
  padding: 10px 25px;
}

@media screen and (max-width: 1022px) {
  .sobre-content {
    flex-direction: column;
  }

  .sobre-content #resumo-sobre {
    object-fit: cover;
    object-position: center;
    width: 100%;
    margin: 0px;
    height: 200px;
  }
}

@media screen and (max-width: 360px) {
  .sobre-content .sobre-pane {
    padding: 20px;
  }
}

@media screen and (max-width: 280px) {
  .sobre-titulo {
    font-size: 2.6rem;
  }
}
</style>