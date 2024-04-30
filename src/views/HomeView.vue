<template>
  <div class="home">
    <div class="geometric-form-1"></div>
    <div class="geometric-form-2"></div>
    <section class="d-flex flex-column align-responsive z-index">
      <h1><strong>Desarrolladora</strong></h1>
      <h1><strong>Front-end</strong></h1>
      <p class="text-home">Me apasiona crear productos front-end sólidos y escalables, brindando experiencias de usuario excepcionales.</p>
      <a class="mt-3" href="#projects"><button class="btn btn-action mb-3">Mis proyectos</button></a>
    </section>
    <section class="d-flex justify-content-center flex-direction-mobile">
      <img class="border-50 img-responsive" src="../assets/images/yo.jpg" alt="Imagen mia" width="350px">
    </section> 
  </div>
</template>

<script>
export default {
  name: 'HomeView',
  methods: {
    
  }
}
</script>
<style>
.home {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 3rem;
}
.text-home {
  width: 50%;
  text-align: left;
}
.home p {
  margin-bottom: 0;
}
.img-responsive {
  max-width: 100%;
  height: auto;
  transition: transform 0.3s ease-in-out;
}
.img-responsive:hover {
  transform: scale(1.1);
}
.border-50 {
  border-radius: 50%;
}
.align-responsive {
  align-items: baseline;
}

.geometric-form-1 {
  width: 65%;
  height: 140%;
  position: absolute;
  top: -10%;
  left: -15%;
  background: linear-gradient(#c50a58, #4a53a8);
  border-radius: 0 50% 50% 0;
  opacity: 0.8;
  box-shadow: 0 1rem 5rem rgba(0, 0, 0, 0.5);
  animation: pulseForm1 3s ease-in-out infinite; /* Añadir animación */
}

.geometric-form-2 {
  width: 70%;
  height: 130%;
  position: absolute;
  top: -10%;
  left: -25%;
  background: linear-gradient(#3646c675, #f4dbe58c 40%);
  opacity: 0.8;
  border-radius: 0 50% 50% 0;
  box-shadow: 0 1rem 5rem rgba(0, 0, 0, 0.5);
  animation: pulseForm2 4s ease-in-out infinite; /* Añadir animación */
}

/* Definir las animaciones */
@keyframes pulseForm1 {
  0% { transform: scale(0.9); }
  50% { transform: scale(1); }
  100% { transform: scale(0.9); }
}

@keyframes pulseForm2 {
  0% { transform: scale(0.8); }
  50% { transform: scale(1); }
  100% { transform: scale(0.8); }
}
.z-index {
  z-index: 1;
}
@media screen and (max-width: 768px) { 
  .flex-direction-mobile, .home {
    flex-direction: column;
  }
  .home {
    height: auto;
    margin-top: 4rem;
  }
  .align-responsive {
    align-items: center;
  }
  .text-home {
    width: 100%;
    text-align: center;
  }
  .img-responsive {
    padding: 1rem;
  }
  .geometric-form-1, .geometric-form-2 {
    display: none;
  }
}
</style>
