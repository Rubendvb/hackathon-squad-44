<template>
  <div>
    <div class="container">
      <div class="row ">
        <div class="col-6 mx-auto mb-4 mt-5 ">
          <div class="mx-auto navTamanho">
            <a class="mx-auto fonteLogo navbar-brand" href="index.html">
              <p class="fonteLogo setarMargin">Mochila cheia</p>
              <router-link to="/"
                ><img
                  class="logo ms-4"
                  src="../assets/imgs/logo.svg"
                  alt="Mochila Cheia"
              /></router-link>
            </a>
          </div>
        </div>
      </div>
    </div>
    <!-- NavBar -->
    <div class="container">
      <div class="row">
        <ul class="nav nav-tabs ">
          <div class="col-3">
            <li class="nav-item">
              <router-link to="/">
                <a class="nav-link" href="">Inicio</a></router-link
              >
            </li>
          </div>
          <div class="col-3">
            <router-link to="/nossacausa">
              <li class="nav-item">
                <a class="nav-link" href="">Nossa Causa</a>
              </li>
            </router-link>
          </div>
          <div class="col-3">
            <router-link to="/contato">
              <li class="nav-item"></li>
              <a class="nav-link" href="">Contato</a></router-link
            >
          </div>
          <div class="col-3">
            <router-link to="/login">
              <li class="nav-item px-2 mt-1">
                <a
                  class="btn verdeLetra btn-outline-primary ml-md-2 mb-2 px-2a"
                  href="/login.vue"
                  >LOGIN</a
                >
              </li>
            </router-link>
          </div>
        </ul>
      </div>
    </div>
    <!-- NavBar -->
    <main>
      <section class="conatiner ">
        <div class="row">
          <div class="col-12 ms-2 pt-5 pb-5 text-center ">
            <h2 class="manrope h2Index mx-auto">
              Entre em contato com o projeto Mochila Cheia
            </h2>
          </div>
        </div>
      </section>
      <section class="conatiner ">
        <div class="row">
          <div class="col-6 mx-auto pt-5">
            <p class="manrope2 mb-5 text-start">
              Tem alguma duvida, sugestão ou quer falar diretamente com a gente?
              Aqui embaixo está os nossos meios de contato.
            </p>
          </div>
        </div>
      </section>
      <section class="conatiner ">
        <div class="row">
          <div class="col-6 mx-auto  ">
            <p class="manrope2 mb-5 text-start">
              <img src="../assets/imgs/email.svg" alt="" />
              projetomcheia@gmail.com
            </p>
          </div>
        </div>
      </section>
      <section class="conatiner ">
        <div class="row">
          <div class="col-6 mx-auto  mb-5">
            <p class="manrope2 mb-5 text-start">
              <img src="../assets/imgs/tel.svg" alt="" /> (13) 15253-0599
            </p>
          </div>
        </div>
      </section>
    </main>
    <div class=" container-fluid backVerde">
      <div class="container">
        <div class="row">
          <p class="copy roxoLetra pt-3 mx-auto">
            © 2021 Mochila Cheia. Todos os direitos reservados
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style></style>
