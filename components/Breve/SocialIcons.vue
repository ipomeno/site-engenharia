<template>
  <div class="social-icons">
    <a href="javascript:void(0)" class="social-icon">
      <i class="fab fa-whatsapp"></i>
    </a>

    <a href="javascript:void(0)" class="social-icon">
      <i class="fab fa-facebook"></i>
    </a>

    <a href="javascript:void(0)" class="social-icon">
      <i class="fab fa-instagram"></i>
    </a>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.social-icons {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.social-icon {
  width: 50px;
  height: 50px;
  background-color: var(--primary-color);
  color: var(--white-color);
  font-size: 25px;
  display: flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  margin: 10px;
  border-radius: 7px;
}

.social-icon:hover {
  background-color: var(--secondary-color);
}
</style>