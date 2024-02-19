<template>
  <div class="home">
    <section class="d-flex justify-content-center flex-column align-items-center p-3">
      <h1>Desarrolladora web</h1>
      <h6>Front end</h6>
      <h6 class="mb-0">Diseño de paginas web UX/UI</h6>
      <section class="d-flex justify-content-center flex-direction-mobile">
        <img src="../assets/images/home.png" class="img-responsive" alt="Imagen de progrmación" width="450px"/>
        <img src="../assets/images/work.png" class="img-responsive" alt="Trabajo" width="450px">
      </section>
    </section>   
    <div class="card margin-container-card p-3">
      <div class="card-body d-flex justify-content-center flex-column align-items-center">
        <h2 class="mt-3 mb-0">Sobre mí</h2>
        <p class="mt-3 mb-3"> Siempre busco actualizar mis conocimientos para obtener nuevos aprendizajes y alcanzar buenos resultados para mis clientes. Me gusta involucrarme en proyectos personales que me permitan experimentar nuevos conceptos e ideas mientras desarrollo y diseño sitios web. Continuamente aprendo y adquiero nuevas habilidades en función de las demandas y tendencias tecnológicas actuales y futuras en el campo del diseño y desarrollo de aplicaciones web. Me apasiona mi trabajo y ofrezco total atención, dedicación, personalización y calidad a cada proyecto que emprendo como desarrolladora web y diseñadora web.
        </p>
        <img class="border-50 img-responsive" src="../assets/images/yo.jpg" alt="Imagen mia" width="250px">
      </div>
    </div>
    <div class="d-flex align-items-center margin-container-card flex-direction-mobile mt-4 p-3">
      <img class="img-responsive" src="../assets/images/contact.png" alt="Contacto" width="200px">
      <section class="d-flex justify-content-center flex-column align-items-center p-3">
        <h2 class="mt-3 mb-0">Trabaja conmigo</h2>
        <p class="mt-3 mb-3">¿Necesitas el talento y la experiencia justa para llevar tu proyecto al siguiente nivel? Mi enfoque es entender tus objetivos y encontrar la solución perfecta para ti. ¡Estoy aquí para ayudarte! ¡Hablemos y veamos cómo puedo contribuir al éxito de tu proyecto!</p>    
        <button type="button" class="btn btn-action mb-3" @click="viewContact">Contáctame</button>  
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeView',
  methods: {
    viewContact() {
      this.$router.push('/contact')
    }
  }
}
</script>
<style>
.home p {
  margin-bottom: 0;
}
.img-responsive {
  max-width: 100%;
  height: auto;
}
.btn-action {
  background-color: #71598a;
  color: white;
}
.btn-action:hover {
  background-color: none;
  color: #71598a;
  border: 2px solid  #71598a;
}
.fa-linkedin {
  color: #0077B5;
}
.fa-github {
  color: #333;
}
.fa-envelope {
  color: #71598a;
}
.fa-linkedin:hover, .fa-github:hover, .fa-envelope:hover {
 font-size: 2.5em;
}
.margin-container-card {
  margin: 0 10rem;
}
.margin-container-card {
  text-align: center;
}
.border-50 {
  border-radius: 50%;
}
@media screen and (max-width: 768px) { 
  .margin-container-card {
    margin: 0;
  }
  .flex-direction-mobile {
    flex-direction: column;
  }
}
</style>
