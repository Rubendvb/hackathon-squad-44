<template>
  <div>
    <div class="container">
      <div></div>
      <div class="row ">
        <div class="col-6 mx-auto mb-4 mt-5 ">
          <div class="mx-auto navTamanho">
            <a class="mx-auto fonteLogo navbar-brand" href="">
              <p class="fonteLogo setarMargin">Mochila cheia</p>
              <router-link to="/">
                <img
                  class="logo ms-4"
                  src="../assets/imgs/logo.svg"
                  alt="Mochila Cheia"
                />
              </router-link>
            </a>
          </div>
        </div>
      </div>
    </div>
    <!-- BarNav -->
    <div class="container">
      <div class="row">
        <ul class="nav nav-tabs ">
          <div class="col-3">
            <router-link to="/">
              <li class="nav-item">
                <a class="nav-link" href="">Inicio</a>
              </li>
            </router-link>
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
              <li class="nav-item">
                <a class="nav-link " href="">Contato</a>
              </li>
            </router-link>
          </div>
          <div class="col-3">
            <router-link to="/login">
              <li class="nav-item px-2 mt-1">
                <a
                  class="btn  verdeLetra btn-outline-primary ml-md-2 mb-2 px-2a"
                  href=""
                  >Sair</a
                >
              </li>
            </router-link>
          </div>
        </ul>
      </div>
    </div>
    <!-- BarNav -->
    <main>
      <section class="container-sm col-12 ">
        <div class="row">
          <div class=" col-12  pt-5 setarMargin ">
            <h2 class="teste roxoLetra setarPadding mx-auto">
              Bem vindo(a), {{userName}}
            </h2>
          </div>
        </div>
      </section>
      <section class="container-sm col-12 ">
        <div class="row">
          <div class=" container-md col-12  pt-5 setarMargin ">
            <p class="teste roxoLetra setarPadding mx-auto">              
            </p>
          </div>
        </div>
      </section>
      <div class="container">        
        <ul class="nav nav-pills nav-fill">
          <li class="nav-item">
            <router-link to="/contausuario">
              <a class="nav-link " aria-current="page" href=""
                >Doar</a
              ></router-link
            >
          </li>
          <li class="nav-item">
            <router-link to="/contausuariocadastrardoacao">
              <a class="nav-link" href="">Cadastrar estudantes</a></router-link
            >
          </li>
          <li class="nav-item">
            <router-link to="/contausuarioinfo">
              <a class="nav-link active" href="">Infos</a>
            </router-link>
          </li>
        </ul>
      </div>
      <section class="container-sm col-12">
        <form class="row  needs-validation" novalidate>
          <div class="col-md-6 position-relative mt-5">
            <label for="validationTooltip01" class="form-label roxoLetra"
              >Nome</label
            >
            <input
              type="text"
              class="form-control verdeLetra"
              id="validationTooltip01"
              v-value=this.userName
              required
            />
            <div class="valid-tooltip">
              Looks good!
            </div>
          </div>          
          <section class="container-sm col-12 ">
            <div class="col-md-6 position-relative mt-5">
              <label for="validationTooltip02" class="form-label roxoLetra">E-mail</label>
              <input
                type="text"
                class="form-control verdeLetra"
                id="validationTooltip02"
                value=""
                required/>
              <div class="valid-tooltip">
                Looks good!
              </div>
            </div>          
          </section>
        </form>
      </section><br>
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
import Parent from '../service/parent'
import VueCookies from 'vue-cookies'

export default {
  data() {
    return {
      userName: VueCookies.get('user').name,
      userEmail: VueCookies.get('user').name,
      students: {

      }
    }    
  }, 
  mounted() {
      Parent.getById(VueCookies.get('user').parentId).then(resposta => {
        console.log(resposta)
        this.students = resposta.data.dependents
      })
  },
  methods: {
    
  }  
}

</script>

<style>
.px-2a {
  padding-right: 4.5rem !important;
  padding-left: 3.5rem !important;
}
</style>
