<script setup>
import NavbarView from './components/NavbarView.vue'
import HomeView from './components/HomeView.vue'
import ServicesView from './components/ServicesView.vue'
import WorksView from './components/WorksView.vue'
import AboutView from './components/AboutView.vue'
import FooterView from './components/FooterView.vue'
</script>

<template>
  <div class='font-inter'>
    <div class='max-w-5xl mx-auto w-11/12'>
      <NavbarView/>
      <HomeView/>
      <ServicesView/>
      <WorksView/>
      <AboutView/>
      <FooterView/>
    </div>
  </div>
</template>

<style scoped>

</style>
