<template>
  <div class="header-container">
    <div class="header-content">
      <div class="header-content-left">
        <img src="~/assets/img/engenharia-logo-clara.png">
      </div>
      <div class="header-content-right">
        <div class="info-container">
          <div class="info-item">
            <div class="info-icon">
              <i class="fa fa-phone"></i>
            </div>
            <div class="info-content">
              <div class="info-title"> (84) 98888-9966 </div>
              <div class="info-text">Fale conosco</div>
            </div>
          </div>

          <div class="info-item">
            <div class="info-icon">
              <i class="fa fa-envelope"></i>
            </div>
            <div class="info-content">
              <div class="info-title"> contato@engenharia.com.br </div>
              <div class="info-text">Mande sua mensagem</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.header-container {
  background-color: var(--accent-color);
  padding: 20px 0px;
}

.header-content {
  margin: 0 auto;
  width: var(--default-content-width);
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header-content-left {
  width: 30%;
}

.header-content-right {
  width: 70%;
}

.logo-container img {
  width: 100%;
}

.info-container {
  display: flex;
  align-items: center;
  justify-content: flex-end;
}

.info-item {
  display: flex;
  align-items: center;
  margin-left: 30px;
}

.info-item .info-icon {
  padding: 10px;
  border: 2px solid var(--primary-color);
  margin: 10px;
}

.info-item .info-icon i {
  color: var(--primary-color);
  font-size: 1.4rem;
}

.info-item .info-content .info-title {
  color: var(--primary-color);
  font-size: 1.2rem;
  font-weight: 700;
}

.info-item .info-content .info-text {
  font-weight: 500;
  font-size: 1.2rem;
}

@media screen  and (max-width: 1250px) {
  .header-content {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }

  .header-content-left {
    width: 100%;
    text-align: center;
  }

  .header-content-right {
    width: 100%;
  }

  .info-container {
    align-items: center;
    justify-content: center;
  }
}

@media screen  and (max-width: 740px) {
  .info-icon {
    display: none;
  }
}

@media screen  and (max-width: 570px) {
  .info-container {
    display: none;
  }
}
</style>