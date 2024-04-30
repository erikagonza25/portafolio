<template>
    <div class="contact d-flex justify-content-start flex-column align-items-center">
        <h2 class="mb-0 text-decoration-title-contact"><strong>Contacto</strong></h2>
        <small class="custom-small text-white">¡Bienvenido/a a la sección de Contacto! ¿Listo/a para conectar? ¡Estoy aquí para escucharte! Descubre cómo podemos colaborar juntos en emocionantes proyectos de programación y tecnología.</small>
        <div class="card p-4 mt-4 custom-card fade-up" ref="formContainer">
            <div class="card-body">
              <form ref="form" @submit.prevent="sendEmail">
                <div class="form-group">
                  <label for="inputName">Nombre</label>
                  <input type="text" class="form-control" id="inputName" placeholder="Ingrese nombre" name="user_name" v-model="formData.user_name">
                </div>
                <div class="form-group mt-2">
                  <label for="inputEmail">Correo</label>
                  <input type="email" class="form-control" id="inputEmail" placeholder="Ingrese correo" name="user_email" v-model="formData.user_email">
                </div>
                <div class="form-group mt-2">
                  <label for="inputMessage">Mensaje</label>
                  <textarea class="form-control" id="inputMessage" rows="7" placeholder="Ingrese mensaje..." name="message" v-model="formData.message"></textarea>
                </div>
                <div class="mt-3 d-flex justify-content-end">
                  <button type="submit" class="btn btn-action" :disabled="!formIsValid || !!loading">
                    <span v-if="!loading">Enviar</span>
                    <div v-else class="spinner-border spinner-border-sm text-light" role="status">
                      <span class="sr-only">Loading...</span>
                    </div>
                  </button>
                </div>
              </form>    
            </div>
        </div>
    </div>
</template>
<script>
import emailjs from '@emailjs/browser'
import Swal from 'sweetalert2'

export default {
  data() {
    return {
      formData: {
        user_name: '',
        user_email: '',
        message: ''
      },
      loading: false
    }
  },
  computed: {
    formIsValid() {
      return this.formData.user_name && this.formData.user_email && this.formData.message;
    }
  },
  mounted () {
    this.animationForm()
  },
  methods: {
    animationForm() {
      const formContainer = this.$refs.formContainer
      const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('active')
          } else {
            entry.target.classList.remove('active')
          }
        })
      })
      observer.observe(formContainer)
    },
    sendEmail() {
      this.loading = true
      emailjs
        .sendForm('service_hduwng3', 'template_jcgputh', this.$refs.form, {
          publicKey: 'buB2-Zz6HFRmm517J',
        })
        .then(() => {
          this.formData = {}
          Swal.fire({
              title: "Enviado",
              text: "He recibido tu correo electrónico. Nos pondremos en contacto contigo lo más pronto posible.",
              icon: "success"
            })
        })
        .catch((error) => {
          Swal.fire({
              icon: "error",
              title: "Oops...",
              text: error
            })
        })
        .finally(()=> {
          this.loading = false
        })
    }
  }
}
</script>

<style>
.contact {
    padding: 5rem;
    background: linear-gradient(#a23060, #f4dbe58c 70%);
}
.custom-card {
    width: 70%;
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
    padding: 5rem 1rem 1rem 1rem;
  }
  .custom-card {
    width: 100%;
  }
}
</style>