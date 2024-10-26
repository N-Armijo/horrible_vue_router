<script setup>
  import NavBar from '@/components/NavBar.vue'
  import Footer from '@/components/Footer.vue'
  import MediosPago from '@/components/MediosPago.vue'
</script>
<template>
  <NavBar />
  <router-view />
  <MediosPago />
  <Footer />
</template>


