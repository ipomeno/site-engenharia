<template>
  <div class="footer-container">
    <div class="footer-content">

      <div class="footer-item">
        <div class="footer-item-empresa">
          <img src="~~/assets/img/engenharia-logo-clara.png" />
          <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolor iste facere cupiditate ipsum beatae molestiae accusamus.</p>

          <div class="social-icons">
            <a href="#" class="social-icon">
              <i class="fab fa-whatsapp"></i>
            </a>
            <a href="#" class="social-icon">
              <i class="fab fa-facebook"></i>
            </a>
            <a href="#" class="social-icon">
              <i class="fab fa-instagram"></i>
            </a>
          </div>
        </div>
      </div>

      <div class="footer-item">
        <div class="footer-item-contato">
          <h3>Contato</h3>
          <ul>
            <li>
              <i class="fab fa-whatsapp"></i>
              <a href="javascript:void(0)">(84) 98888-7777</a>
            </li>
            <li>
              <i class="fa fa-phone"></i>
              <a href="javascript:void(0)">(84) 98888-7777</a>
            </li>
            <li>
              <i class="fa fa-envelope"></i>
              <a href="javascript:void(0)">contato@engenharia.com.br</a>
            </li>
            <li>
              <i class="fa fa-location-dot"></i>
              <a href="javascript:void(0)">Lorem ipsum dolor sit amet consectetur adipisicing elit obcaecati dolorem.</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer-item">
        <div class="footer-item-links">
          <h3>Links úteis</h3>
          <ul>
            <li>
              <i class="fa fa-chevron-right"></i>
              <a href="javascript:void(0)">Início</a>
            </li>
            <li>
              <i class="fa fa-chevron-right"></i>
              <a href="javascript:void(0)">Sobre</a>
            </li>
            <li>
              <i class="fa fa-chevron-right"></i>
              <a href="javascript:void(0)">Serviços</a>
            </li>
            <li>
              <i class="fa fa-chevron-right"></i>
              <a href="javascript:void(0)">Contato</a>
            </li>
            <li>
              <i class="fa fa-chevron-right"></i>
              <a href="javascript:void(0)">Política de privacidade</a>
            </li>
          </ul>

        </div>
      </div>

      <div class="footer-item">
        <div class="footer-item-localizacao">
          <h3>Localização</h3>
          <div class="maps">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15878.164107054288!2d-35.203855149999995!3d-5.7789664!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x7b30041869ef645%3A0xb9a0cdb1deb6193c!2sNatal%20Praia%20Hotel!5e0!3m2!1spt-BR!2sbr!4v1674052273253!5m2!1spt-BR!2sbr" width="100%" height="150" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade">
            </iframe>
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
.footer-container {
  background-image: url('~~/assets/img/background-rodape.jpg');
  background-position: top right;
  background-size: cover;
  background-repeat: no-repeat;

  background-color: var(--accent-color);
  padding: 100px 0px;
}

.footer-content {
  margin: 0 auto;
  width: var(--default-content-width);

  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 20px;
}

.footer-item {
  width: 25%;
  height: 240px;
  background-color: rgba(255, 255, 255, 0.07);
  padding: 20px;
  border-radius: 10px;
}

.footer-item-empresa img {
  margin-top: -10px;
}

.footer-item-empresa p {
  color: var(--white-transp-color);
  font-size: 0.9rem;
  padding-bottom: 10px;
  margin: 10px 0px;
  text-align: justify;
}

.social-icons {
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

.social-icon {
  padding: 5px 10px;
  background-color: var(--primary-color);
  margin-right: 10px;
}

.social-icon:hover {
  background-color: var(--secondary-color);
}

.social-icon i {
  font-size: 1.2rem;
}

.footer-item-contato h3,
.footer-item-localizacao h3,
.footer-item-links h3 {
  font-weight: 700;
  padding-left: 10px;
  border-left: 1px solid var(--primary-color);
  font-size: 1.2rem;
  margin-bottom: 20px;
}

.footer-item-contato ul li,
.footer-item-links ul li {
  margin: 10px 0px;
  display: flex;
  align-items: center;
}

.footer-item-contato ul li i,
.footer-item-links ul li i {
  color: var(--primary-color);
  font-weight: 700;
  font-size: 1rem;
  margin-right: 10px;
}

.footer-item-links ul li i {
  font-size: 0.7rem;
}

.footer-item-contato ul li a,
.footer-item-links ul li a {
  text-decoration: none;
  color: rgba(255, 255, 255, 0.7);
}

.footer-item-contato ul li a:hover,
.footer-item-links ul li a:hover {
  color: rgba(255, 255, 255, 1);
}


@media screen and (max-width: 1780px) {
  .footer-content {
    flex-wrap: wrap;
  }

  .footer-item:nth-child(1) {
    width: 100%;
    background-color: transparent;
  }

  .footer-item-empresa,
  .footer-item-empresa p {
    text-align: center;
  }

  .footer-item-empresa .social-icons {
    justify-content: center;
  }
  .footer-item:not(:nth-child(1)) {
    width: 32%;
  }
}

@media screen and (max-width: 1120px) {
  .footer-item:last-child {
    width: 100%;
    background-color: transparent;
  }

  .footer-item:not(:first-child):not(:last-child) {
    width: 45%;
    flex-grow: 1;
  }
}

@media screen and (max-width: 685px) {
  .footer-item:not(:first-child):not(:last-child) {
    flex-grow: 0;
    width: 100%;
    background-color: transparent;
  }
}
</style>