<template>
  <div class="d-flex justify-content-center flex-column align-items-center padding-custom">
    <h2 class="mt-3 mb-0 text-decoration-title"><strong>Proyectos</strong></h2>
    <small class="custom-small">¡Bienvenido/a a la sección de proyectos! Descubre algunas de mis contribuciones en el emocionante mundo de la programación y la tecnología.</small>
    <div class="mt-4 d-flex container-cards">
      <div v-for="project in projects" :key="project.id" class="project-card card m-2 fade-up" style="width: 20rem; height: 30rem;">
        <img class="card-img-top" :src="require(`@/${project.img}`)" alt="Card image cap">
        <div class="card-body flex-card">
          <h5 class="card-title">{{ project.name }}</h5>
          <small class="card-text">{{ project.description }}</small>
          <h6 class="mt-1">Tecnologías Utilizadas:</h6>
          <ul class="container-skills mb-1">
            <li v-for="(skill, index) in project.skills" :key="index">
              <i v-if="!skill.svg" :class="['fa-brands', 'skills-projects', skill.name]" :style="{ color: skill.color }"></i>
              <svg v-if="!!skill.svg && skill.name === 'styled-components'" fill="#000000" width="50px" height="50px" viewBox="0 0 24 24" role="img" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><title>styled-components icon</title><path d="M16.214 6.762l-.075.391c-.116.741-.074.953.244 1.228l.307.254-.318 1.418c-.19.846-.423 1.555-.571 1.788-.127.201-.275.497-.307.656-.053.19-.233.381-.508.55-.243.138-.72.508-1.058.805-.27.243-.456.392-.557.456l-.33.261c-.106.17-.166.307-.189.411-.023.107-.01.178.024.23.033.05.09.085.168.107a.954.954 0 00.282.023 3 3 0 00.632-.112c.07-.019.125-.037.173-.053.074-.091.245-.263.548-.562.804-.793 1.111-1.227.794-1.11-.117.042-.064-.064.137-.276.424-.413.667-1.037 1.175-2.994.402-1.545.402-1.567.698-1.567.139 0 .532.024.532.024V6.762h-.902zm3.839 3.165c-.064 0-.17.096-.233.202-.116.19.021.306 1.767 1.396 1.037.657 1.873 1.217 1.852 1.26-.021.031-.868.582-1.883 1.217-1.842 1.142-1.852 1.153-1.683 1.386.212.275 0 .37 2.391-1.122L24 13.155v-.836l-1.937-1.196c-1.047-.656-1.957-1.185-2.01-1.196zm-16.085.117c-.053 0-.963.54-2.01 1.185L0 12.425v.836l1.947 1.217c1.08.666 1.99 1.217 2.032 1.217.042 0 .127-.096.212-.212.127-.201.02-.286-1.768-1.418C.72 12.996.54 12.848.71 12.732c.106-.074.91-.572 1.778-1.111 1.979-1.217 1.873-1.133 1.714-1.387-.063-.105-.17-.2-.233-.19zm8.684.023c-.292-.002-.92.443-2.8 1.978-.081.193-.088.326-.051.412.024.059.068.1.129.13.06.03.138.048.224.055.171.015.373-.012.536-.044l.11-.025a.386.386 0 01.144-.118c.116-.064.603-.508 1.09-.984.857-.868 1.058-1.26.709-1.387a.24.24 0 00-.09-.017zm2.196.603c-.257.007-.72.305-1.513.938-.398.323-.65.497-.785.533l-.524.414c-.197.36-.226.583-.174.706a.25.25 0 00.138.134.644.644 0 00.24.045 2.18 2.18 0 00.58-.085 3.466 3.466 0 00.291-.092l.029-.012.053-.028c.1-.129.33-.372.618-.652.91-.878 1.375-1.502 1.28-1.735-.043-.113-.117-.17-.233-.166zm-2.424 1.08c-.074.008-.24.136-.539.398-.432.382-.903.602-1.066.504a3.97 3.97 0 01-.114.024c-.166.033-.373.06-.558.045a.708.708 0 01-.252-.063.337.337 0 01-.168-.17c-.037-.09-.037-.202.005-.345l-.65.534-1.471 1.217V15.867l4.82-3.797a.41.41 0 01.016-.123c.037-.134.035-.202-.023-.196zm2.074.639c-.073 0-.195.103-.39.31-.265.283-.682.557-.903.613l-.034.018a2.191 2.191 0 01-.11.042c-.06.02-.138.044-.228.068-.18.049-.404.094-.604.089a.732.732 0 01-.275-.054.344.344 0 01-.184-.18c-.058-.139-.035-.334.092-.611L7.61 16.033v1.205h1.868l3.962-3.112c.103-.114.258-.27.467-.465.56-.519.687-.698.687-.963 0-.206-.023-.31-.096-.31zm.943 1.95l-.339.338c-.19.18-.529.402-.761.497l-.046.02-.003.005-.01.01c-.009.007-.013.008-.02.011a3.432 3.432 0 01-.282.093 3.058 3.058 0 01-.65.115 1.035 1.035 0 01-.31-.027.364.364 0 01-.218-.144c-.048-.074-.062-.173-.035-.295a1.11 1.11 0 01.095-.25l-3.197 2.526h4.252l.508-.582c.698-.814 1.016-1.396 1.016-1.894z"></path></g></svg>
              <svg v-if="!!skill.svg && skill.name === 'firebase'" width="50px" height="50px" viewBox="0 0 32 32" xmlns="http://www.w3.org/2000/svg" fill="#000000"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"><title>file_type_firebase</title><path d="M5.8,24.6l.17-.237L13.99,9.149l.017-.161L10.472,2.348a.656.656,0,0,0-1.227.207Z" style="fill:#ffc24a"></path><path d="M5.9,24.42l.128-.25L13.965,9.114,10.439,2.448a.6.6,0,0,0-1.133.206Z" style="fill:#ffa712"></path><path d="M16.584,14.01l2.632-2.7L16.583,6.289a.678.678,0,0,0-1.195,0L13.981,8.971V9.2Z" style="fill:#f4bd62"></path><path d="M16.537,13.9l2.559-2.62L16.537,6.4a.589.589,0,0,0-1.074-.047L14.049,9.082l-.042.139Z" style="fill:#ffa50e"></path><polygon points="5.802 24.601 5.879 24.523 6.158 24.41 16.418 14.188 16.548 13.834 13.989 8.956 5.802 24.601" style="fill:#f6820c"></polygon><path d="M16.912,29.756,26.2,24.577,23.546,8.246A.635.635,0,0,0,22.471,7.9L5.8,24.6l9.233,5.155a1.927,1.927,0,0,0,1.878,0" style="fill:#fde068"></path><path d="M26.115,24.534,23.483,8.326a.557.557,0,0,0-.967-.353L5.9,24.569l9.131,5.1a1.912,1.912,0,0,0,1.863,0Z" style="fill:#fcca3f"></path><path d="M16.912,29.6a1.927,1.927,0,0,1-1.878,0L5.876,24.522,5.8,24.6l9.233,5.155a1.927,1.927,0,0,0,1.878,0L26.2,24.577l-.023-.14Z" style="fill:#eeab37"></path></g></svg>
            </li> 
          </ul>
          <a :href="project.url" class="btn btn-action" target="_blank">Visita la página</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: 1, 
          name: 'Marvel Database', 
          description: 'Marvel Database es una plataforma dedicada al universo de Marvel, donde los entusiastas pueden explorar datos detallados de los personajes, buscar por nombre y personalizar localmente la información.',
          skills: [
            {name : 'fa-html5', color: '#e44d26'},
            {name : 'fa-css3-alt', color: '#264de4'},
            {name : 'fa-js', color: '#f0db4f'},
            {name : 'fa-react', color: '#61dafb'},
            {name : 'fa-github', color: '#333'},
            {name : 'styled-components', color: '#000', svg: true}
          ],
          url: 'https://marvel-api-omega.vercel.app/',
          img: 'assets/images/marvel.png'
        },
        {
          id: 2, 
          name: 'Rick and Morty Universe', 
          description: 'Explora el universo de la serie Rick and Morty con nuestra página web, donde podrás acceder a datos detallados de los personajes, filtrarlos según tus preferencias y buscarlos por nombre.',
          skills: [
            {name : 'fa-html5', color: '#e44d26'},
            {name : 'fa-css3-alt', color: '#264de4'},
            {name : 'fa-js', color: '#f0db4f'},
            {name: 'fa-sass', color: '#cd6799'},
            {name : 'fa-vuejs', color: '#41b883'},
            {name : 'fa-github', color: '#333'}
          ],
          url: 'https://rick-and-morty-erika.netlify.app/',
          img: 'assets/images/rick.png'
        },
        {
          id: 3, 
          name: 'Burger Queen Ordering System', 
          description: 'Burger Queen te trae una interfaz intuitiva para tomar pedidos utilizando una tablet y enviarlos a la cocina de manera ordenada y eficiente.',
          skills: [
            {name : 'fa-html5', color: '#e44d26'},
            {name : 'fa-css3-alt', color: '#264de4'},
            {name : 'fa-js', color: '#f0db4f'},
            {name: 'fa-sass', color: '#cd6799'},
            {name : 'fa-react', color: '#61dafb'},
            {name : 'fa-github', color: '#333'},
            {name : 'fa-figma', color: '#333333'},
            {name : 'firebase', color: '#000', svg: true}
          ],
          url: 'https://burger-queen-a6754.web.app/',
          img: 'assets/images/burger.png'
        },
        {
          id: 4, 
          name: 'Wartay - Red Social Interactiva', 
          description: 'Wartay es una plataforma social dinámica que te permite crear una cuenta, iniciar sesión y disfrutar de funciones completas para interactuar con otros usuarios. ¡Crea, edita, borra y da "me gusta" a publicaciones!',
          skills: [
            {name : 'fa-html5', color: '#e44d26'},
            {name : 'fa-css3-alt', color: '#264de4'},
            {name : 'fa-js', color: '#f0db4f'},
            {name : 'fa-github', color: '#333'},
            {name : 'fa-figma', color: '#333333'},
            {name : 'firebase', color: '#000', svg: true}
          ],
          url: 'https://erikagonza25.github.io/LIM014-social-network/',
          img: 'assets/images/wartay.png'
        },
        {
          id: 5, 
          name: 'League of Legends Hub', 
          description: 'Explora el mundo de League of Legends con nuestra página web dedicada, donde puedes acceder a datos detallados de los campeones, filtrarlos, ordenarlos y obtener estadísticas promedio basadas en niveles de dificultad.',
          skills: [
            {name : 'fa-html5', color: '#e44d26'},
            {name : 'fa-css3-alt', color: '#264de4'},
            {name : 'fa-js', color: '#f0db4f'},
            {name : 'fa-github', color: '#333'},
            {name : 'fa-figma', color: '#333333'},
          ],
          url: 'https://erikagonza25.github.io/LIM014-data-lovers/',
          img: 'assets/images/league.png'
        },
        {
          id: 6, 
          name: 'Validación de Tarjeta de Crédito', 
          description: 'Asegura tus transacciones con nuestra herramienta de validación de tarjetas de crédito, que verifica la autenticidad de las tarjetas antes de realizar cualquier transacción de cobro.',
          skills: [
            {name : 'fa-html5', color: '#e44d26'},
            {name : 'fa-css3-alt', color: '#264de4'},
            {name : 'fa-js', color: '#f0db4f'},
            {name : 'fa-github', color: '#333'},
            {name : 'fa-figma', color: '#333333'},
          ],
          url: 'https://card-validation-erika.vercel.app/',
          img: 'assets/images/card.png'
        }
      ]
    }
  },
  mounted () {
    this.animationForm()
  },
  methods: {
    animationForm() {
      const cards = document.querySelectorAll('.fade-up')
      const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('active')
          } else {
            entry.target.classList.remove('active')
          }
        })
      })

      cards.forEach(card => {
        observer.observe(card)
      })
    }
  }
}
</script>

<style>
.container-cards {
  max-width: 100%;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}
.container-skills{
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  margin-top: 1rem;
  margin: 0;
  padding: 0;
}
.container-skills li {
  list-style: none;
}
.skills-projects {
    font-size: 2rem;
    margin: 0.4rem
}
.flex-card {
  justify-content: space-evenly;
  display: flex;
  flex-direction: column;
  align-items: baseline;
}
.card-text {
  font-weight: 400;
}
.fade-up {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 1s ease, transform 1s ease;
}

.fade-up.active {
  opacity: 1;
  transform: translateY(0);
}
@media screen and (max-width: 768px) { 
  .project-card {
    height: 100% !important;  
  }
}

</style>
  
  