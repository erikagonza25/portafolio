<template>
    <nav class="navbar navbar-expand-lg fixed-top">
        <div class="container-fluid">
            <a class="navbar-brand" href="#"><router-link to="/"><img src="@/assets/images/logo.png" alt="logo" width="45px"></router-link></a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
            <ul class="navbar-nav">
                <li v-for="(option, index) in navOptions" :key="index" class="nav-item">
                    <router-link :class="{ 'nav-link': true, 'active': option.active }" :to="option.to">{{ option.text }}</router-link>
                </li>
            </ul>
            </div>
        </div>
    </nav>
</template>
<script>
export default {
  data() {
    return {
      navOptions: [
        { text: 'Inicio', to: '/', active: true },
        { text: 'Contacto', to: '/contact', active: false },
        { text: 'Mis proyectos', to: '/projects', active: false }
      ]
    };
  }
}
</script>
<style>
.fixed-top {
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1000;
  background-color: #77777726; 
  padding: 0.2rem !important;
}
.navbar-brand a {
    border-bottom: 0 !important;
}
.nav-link {
    color: black !important;
}
nav a.router-link-exact-active {
  color: #71598a !important;
  border-bottom: 2px solid #71598a;
  font-weight: 500;
}
</style>