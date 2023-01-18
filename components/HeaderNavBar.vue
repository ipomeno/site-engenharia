<template>
  <div class="navbar-container">
    <div class="navbar-content">
      <a href="javascript:void(0)" class="menu-btn" @click="btnMenuMobileOnClick($event)">
        <i class="fa fa-bars"></i>
      </a>

      <ul class="menu">
        <li><a href="#">Início</a></li>
        <li><a href="#">Sobre</a></li>
        <li><a href="#">Serviços</a></li>
        <li><a href="#">Contato</a></li>
      </ul>
      <div class="social-menu">
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
  </div>
</template>

<script>
export default {
  methods: {
    btnMenuMobileOnClick(event) {
      let menu = this.$el.querySelector('.menu');
      let icon = this.$el.querySelector('.menu-btn i');

      if (!menu.classList.contains('menu-show')) {
        menu.classList.add('menu-show');
        icon.setAttribute('class', 'fa fa-times');
        return;
      }

      menu.classList.remove('menu-show');
      icon.setAttribute('class', 'fa fa-bars');
    }
  }
}
</script>

<style scoped>
.navbar-container {
  background-color: var(--primary-color);

  /** scroll do menu */
  position: sticky;
  top: 0;
  z-index: 30;
}

.navbar-content {
  margin: 0 auto;
  width: var(--default-content-width);
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: relative;
}

.menu {
  list-style-type: none;
  display: flex;
  align-items: center;
}

.menu li a {
  text-decoration: none;
  padding: 15px 30px;
  display: block;
  font-weight: 500;
}

.menu li a:hover {
  background-color: var(--secondary-color);
}

.social-icons {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.social-icon {
  padding: 10px 20px;
}

.social-icon:hover {
  background-color: var(--secondary-color);
}

.social-icon i {
  font-size: 1.6rem;
}

.menu-btn {
  padding: 10px 15px;
  display: none;
}

.menu-btn:hover {
  background-color: var(--secondary-color);
}

@media screen and (max-width: 1235px) {
  .navbar-content {
    width: 80%;
  }
}

@media screen and (max-width: 800px) {
  .navbar-content {
    width: 100%;
    padding: 0px 10px;
  }
  .menu-btn {
    display: block;
  }

  .menu {
    display: none;
    width: 100%;
    background-color: var(--primary-color);
    flex-direction: column;
    position: absolute;
    left: 0;
    top: 45px;
  }

  .menu-show {
    display: flex;
  }

  .menu li,
  .menu li a {
    width: 100%;
  }
}
</style>