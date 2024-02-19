<template>
    <footer class="p-2 d-flex justify-content-around">
      <p class="mb-0">Conéctame en las redes sociales:</p>
      <section>
        <a href="https://github.com/erikagonza25" target="_blank"><i class="fa-brands fa-github fa-2xl"></i></a>
        <a href="https://www.linkedin.com/in/erika-gonzalez-nunez/" target="_blank"><i class="fa-brands fa-linkedin fa-2xl"></i></a>
        <a :href="'mailto:' + emailAddress">
          <i class="fas fa-envelope fa-2xl"></i>
        </a>
      </section>
    </footer>
</template>
<script>
export default {
  name: 'TheFooter',
  data () {
    return {
    emailAddress: 'erikagonza2013@gmail.com'
    }
  }
}
</script>
<style>
footer {
  background-color: #77777726; 
}
footer a {
  margin-right: 1rem;
}
footer p {
  font-weight: 600;
}
</style>