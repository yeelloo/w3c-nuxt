<template>
  <div class="layout-wrapper">
    <MainMenu />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import MainMenu from '~/components/MainMenu.vue'
import Footer from '~/components/Footer/Footer.vue'
export default{
  components: {
    MainMenu, Footer
  }
}
</script>

<style>

</style>
