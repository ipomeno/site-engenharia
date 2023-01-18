<template>
  <div class="container">
    <div class="container-row">
      <div class="body-text">
        <h2>Solicite seu orçamento</h2>
        <hr/>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Id explicabo repudiandae corrupti non doloremque temporibus minima fuga. Quasi, dolor iste beatae doloribus, porro itaque voluptates, ad perspiciatis et odit laudantium.</p>
      </div>
      <div class="button-container">
        <a href="javascript:void(0);" class="btn-saiba-mais">Peça seu orçamento</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  background-color: var(--primary-color);
  padding: 100px 0px;
}

.container-row {
  text-align: center;
  margin: 0px auto;
  width: var(--default-content-width);
}

h2 {
  color: var(--white-color);
  font-weight: 800;
  font-size: 3.5rem;
}

hr {
  border-color: var(--accent-color);
  border-width: 2px;
  width: 10%;
  margin: 30px auto;
}

.button-container {
  margin-top: 30px;
}

.btn-saiba-mais {
  text-transform: uppercase;
  background-color: rgba(3, 15, 39, 0.6);
  font-weight: 700;
}

.btn-saiba-mais:hover {
  background-color: var(--accent-color);
}

@media screen and (max-width: 290px) {

  h2 {
    font-weight: 800;
    font-size: 2.6rem;
  }
  
}
</style>