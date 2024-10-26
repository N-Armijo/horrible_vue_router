<script setup>
  import { useRouter } from 'vue-router'

  //accede router
  const router = useRouter()
  //navegar inicio
  const volverAlInicio = () => {
    router.push({ name: 'inicio' })
  }
</script>
<template>
  <div class="container">
    <div class="row">
      <div class="col-12 p-5">
        <h1 class="p-5 text-center">Contacto</h1>
        <button @click="volverAlInicio" class="btn btn-primary col-12">Ir a Inicio</button>
      </div>
    </div>
  </div>
</template>
