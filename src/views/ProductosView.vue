<script setup>
  import { defineProps } from 'vue'
  import { useRouter } from 'vue-router'
  import SingleCard from '../components/SingleCard.vue'
  //propiedades del componente
  const props = defineProps({
    nombre: {
      type: String,
      required: true
    },
    descripcion: {
      type: String,
      required: true
    },
    precio: {
      type: Number,
      required: true
    },
    cantidad: {
      type: String,
      required: true
    }
  })
  // accede al router
  const router = useRouter()
  //navegar al inicio
  const volverAlInicio = () => {
    router.push({ name: 'inicio' })
  }
</script>
<template>
  <section class="container" id="productos">
    <h1 class="text-center">Nuestros Productos</h1>
    <div class="row">
      <div class="col-sm-4 col-12 px-5 mb-4">
        <SingleCard
          :nombre="nombre"
          :descripcion="descripcion"
          :precio="precio"
          :cantidad="cantidad"
        />
      </div>
    </div>
    <div class="row">
      <button @click="volverAlInicio" class="btn btn-primary mb-4">Ir a Inicio</button>
    </div>
  </section>
</template>


