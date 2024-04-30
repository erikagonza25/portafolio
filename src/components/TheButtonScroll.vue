<template>
    <div class="bottonScroll" v-show="showButton" @click="scrollToTop">
      <i class="fa-solid fa-circle-chevron-up"></i>
    </div>
  </template>
  
<script>
export default {
  data() {
    return {
      showButton: false
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      if (window.pageYOffset > 200) {
        this.showButton = true
      } else {
        this.showButton = false
      }
    },
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      })
    }
  }
}
</script>

<style>
.bottonScroll {
  position: fixed;
  bottom: 50px;
  right: 50px;
  cursor: pointer;
  opacity: 1;
  transition: opacity 0.3s;
}

.bottonScroll i {
  color: #612485;
  font-size: 60px;
}
</style>
