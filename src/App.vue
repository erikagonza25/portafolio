<template>
  <div>
    <TheNavBar/>
    <router-view class="margin-container"/>
    <TheFooter/>
  </div>
</template>

<script>
import TheNavBar from './components/TheNavBar.vue'
import TheFooter from './components/TheFooter.vue'
export default  {
  name: 'app',
  components: {TheNavBar, TheFooter}
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
</style>
