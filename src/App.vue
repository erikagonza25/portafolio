<template>
  <div>
    <TheNavBar/>
    <HomeView class="section" id="home"/>
    <AboutView class="section" id="about"/>
    <ProjectsView class="section" id="projects"/>
    <ContactView class="section" id="contact"/>
    <TheButtonScroll/>
    <TheFooter/>
  </div>
</template>

<script>
import HomeView from './views/HomeView.vue'
import AboutView from './views/AboutView.vue'
import ProjectsView from './views/ProjectsView.vue'
import ContactView from './views/ContactView.vue'
import TheNavBar from './components/TheNavBar.vue'
import TheFooter from './components/TheFooter.vue'
import TheButtonScroll from './components/TheButtonScroll.vue'
export default  {
  name: 'app',
  components: {TheNavBar, TheFooter, ContactView, HomeView, AboutView, ProjectsView, TheButtonScroll}
}
</script>
<style>
body {
  margin: 0;
  padding: 0;
  font-family: "Fredoka", sans-serif !important;
  background: linear-gradient(80deg, rgba(238,174,202,1) 0%, rgba(242,234,251,1) 100%);
}
.margin-container {
  margin-top: 5rem;
}
.text-decoration-title{
  border-bottom: 3px solid #71598a;
}
.padding-custom {
    padding: 4rem;
}
.btn-action {
  background-color: #000 !important;
  color: white !important;
}
.btn-action:hover {
  box-shadow: 1px 4px 5px 0px rgba(0,0,0,0.44);
}
.custom-small {
  text-align: center;  
  width: 50%;
  margin: 0.5rem 0;
}
@media screen and (max-width: 768px) { 
  .padding-custom {
    padding: 4rem 1rem 1rem 1rem;
  }
  .custom-small { 
   width: 100%;
  }
}

</style>
