<template>
    <nav class="navbar navbar-expand-lg fixed-top" :class="activeSection !== 'home' ? 'bg-white' : ''">
        <div class="container-fluid">
            <a class="navbar-brand" href="#home"><img src="@/assets/images/logo.png" alt="logo" width="45px"></a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
            <ul class="navbar-nav">
              <li><a :class="{ 'nav-link': true, 'active': activeSection === 'home' }" href="#home">Inicio</a></li>
              <li><a :class="{ 'nav-link': true, 'active': activeSection === 'about' }" href="#about">Acerca de mi</a></li>
              <li><a :class="{ 'nav-link': true, 'active': activeSection === 'projects' }" href="#projects">Proyectos</a></li>
              <li><a :class="{ 'nav-link': true, 'active': activeSection === 'contact' }" href="#contact">Contacto</a></li>
            </ul>
            </div>
        </div>
    </nav>
</template>
<script>
export default {
  name: 'App',
  data() {
    return {
      activeSection: 'home'
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
    this.handleScroll()
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      const sections = document.querySelectorAll('.section')
      let currentSection = ''
      sections.forEach(section => {
        const rect = section.getBoundingClientRect()
        if (rect.top <= 70 && rect.bottom >= 70) {
          currentSection = section.id
        }
      })
      this.activeSection = currentSection || 'home'
    }
  }
};
</script>
<style>
.fixed-top {
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1000;
  padding: 0.5rem !important;
}
.bg-white {
  background-color: #fff; 
}
.navbar-brand, .nav-link {
  margin: 0
}
.navbar-brand a {
    border-bottom: 0 !important;
}
.nav-link {
    color: black !important;
}
.active {
  border-bottom: 2px solid #71598a !important;
  font-weight: 500 !important;
}
</style>