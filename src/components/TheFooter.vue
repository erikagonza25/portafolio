<template>
    <footer class="d-flex justify-content-around flex-direction-mobile align-items-center">
      <section>
        <p class="mb-0">¡Sígueme en las redes sociales y descubre más sobre mi trabajo!</p>
        <p class="margin-mobile-bottom">Estoy emocionado/a de conectarme contigo:</p>
      </section> 
      <section>
        <a href="https://github.com/erikagonza25" target="_blank"><i class="fa-brands fa-footer fa-github fa-2xl"></i></a>
        <a href="https://www.linkedin.com/in/erika-gonzalez-nunez/" target="_blank"><i class="fa-brands fa-footer fa-linkedin fa-2xl"></i></a>
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
  background-color: #fff; 
  padding: 1rem;
}
footer a {
  margin-right: 1rem;
}
footer p {
  font-weight: 400;
}

.fa-linkedin {
  color: #0077B5;
}
.fa-github {
  color: #333;
}
.fa-footer:hover{
 font-size: 2.5em;
}
.margin-mobile-bottom {
  margin-bottom: 0;
}
@media screen and (max-width: 768px) { 
  .flex-direction-mobile {
    flex-direction: column;
  }
  .margin-mobile-bottom {
    margin-bottom: 1rem;
  }
}
</style>