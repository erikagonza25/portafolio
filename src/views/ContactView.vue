<template>
    <div class="contact d-flex justify-content-start flex-column align-items-center">
        <h2 class="mb-0 text-decoration-title-contact"><strong>Contacto</strong></h2>
        <small class="custom-small text-white">¡Bienvenido/a a la sección de Contacto! ¿Listo/a para conectar? ¡Estoy aquí para escucharte! Descubre cómo podemos colaborar juntos en emocionantes proyectos de programación y tecnología.</small>
        <div class="card p-4 mt-4 custom-card fade-up">
            <div class="card-body">
                <form>
                    <div class="form-group">
                        <label for="exampleName">Nombre</label>
                        <input type="text" class="form-control" id="exampleName" placeholder="Enter name">
                    </div>
                    <div class="form-group">
                        <label for="exampleInputEmail1">Email address</label>
                        <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
                        <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
                    </div>
                    <div class="form-group">
                        <label for="exampleName">Number</label>
                        <input type="text" class="form-control" id="exampleName" placeholder="Enter number">
                    </div>
                    <div class="form-group">
                        <label for="exampleFormControlTextarea1">Example textarea</label>
                        <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
                    </div>
                    <div class="form-check">
                        <input type="checkbox" class="form-check-input" id="exampleCheck1">
                        <label class="form-check-label" for="exampleCheck1">Check me out</label>
                    </div>
                    <button type="submit" class="btn btn-primary">Submit</button>
                </form>      
            </div>
        </div>
    </div>
</template>
<script>
export default {
  mounted () {
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
</script>

<style>
.contact {
    padding: 5rem;
    background: linear-gradient(#a23060, #f4dbe58c 70%);
}
.custom-card {
    width: 50%;
}
.text-decoration-title-contact, .text-white {
    color: #fff;
}
.text-decoration-title-contact{
  border-bottom: 3px solid #fff;
}
.fade-up {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 1.5s ease, transform 1.5s ease;
}

.fade-up.active {
  opacity: 1;
  transform: translateY(0);
}
@media screen and (max-width: 768px) { 
  .contact {
    padding: 1rem;
  }
  .custom-card {
    width: 100%;
  }
}
</style>