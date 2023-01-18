<template>
  <div class="categorias-container">
    <div class="categorias-content">

      <div class="categoria-box">
        <div class="categoria-box-icon">
          <i class="fa fa-edit"></i>
        </div>
        <h1 class="categoria-box-title">Atendimento <br />Personalizado</h1>
        <p class="categoria-box-text">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur corporis quod dignissimos veniam nisi.
        </p>
      </div>

      <div class="categoria-box categoria-single-border">
        <div class="categoria-box-icon">
          <i class="fa fa-edit"></i>
        </div>
        <h1 class="categoria-box-title">Profissionais<br />Qualificados</h1>
        <p class="categoria-box-text">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur corporis quod dignissimos veniam nisi.
        </p>
      </div>

      <div class="categoria-box">
        <div class="categoria-box-icon">
          <i class="fa fa-edit"></i>
        </div>
        <h1 class="categoria-box-title">Tecnologia <br />de Ponta</h1>
        <p class="categoria-box-text">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur corporis quod dignissimos veniam nisi.
        </p>
      </div>

    </div>
  </div>
</template>

<style scoped>
.categorias-container {
  background-color: var(--white-cold-color);
  height: 240px;
}

.categorias-container .categorias-content {
  margin: 0 auto;
  width: var(--default-content-width);
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-top: 3px solid var(--primary-color);
  background-color: var(--white-color);
  position: relative;
  top: -150px;
  box-shadow: 0px 10px 35px rgba(0, 0, 0, 0.3);
  padding: 50px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.categoria-box {
 color: #000;
 padding: 0px 25px;
 display: flex;
 flex-direction: column;
 align-items: center;
 justify-content: space-between;
 text-align: center;
}

.categoria-box-icon .fa {
  color: var(--primary-color);
  font-weight: 900;
  font-size: 40px;
  margin-bottom: 10px;
}

.categoria-box-title {
  color: var(--accent-color);
  font-weight: 600;
  font-size: 1.3rem;
  margin: 10px 0;
}

.categoria-box-text {
  color: #666;
  font-size: 0.9rem;
  font-weight: 300;
}

.categoria-w30 {
  width: 30%;
}

.categoria-w35 {
  width: 35%;
}

.categoria-single-border {
  border-left: 1px solid var(--white-cold-color);
  border-right: 1px solid var(--white-cold-color); 
}

@media screen and (max-width: 800px) {
  .categorias-container {
    height: 600px;
  }
  .categorias-container .categorias-content {
    width: 70%;
    padding: 50px 10px;
    flex-direction: column;
  }

  .categoria-box {
    padding: 25px;
  }
  
  .categoria-box:nth-child(2) {
    border-left: none;
    border-right: none;
    border-top: 1px solid var(--white-cold-color);
    border-bottom: 1px solid var(--white-cold-color);
  }
}

@media screen and (max-width: 700px) {
  .categorias-container {
    height: 700px;
  }
}

@media screen and (max-width: 400px) {
  .categorias-container {
    height: 800px;
  }
}
</style>