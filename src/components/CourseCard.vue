<template>
    <div class="card h-100 border-0 shadow-sm">
      <div class="card-body p-4">
        <div class="text-center mb-3">
       
          <h3 class="card-title fw-bold fs-5">{{ title }}</h3>
        </div>
        <p class="card-text text-center text-secondary">{{ description }}</p>
        <div v-if="image" class="mt-4">
          <img :src="image" :alt="title" class="img-fluid rounded">
        </div>
      </div>
    </div>
</template>
  
  <script lang="ts">
  import { defineComponent } from 'vue';
  
  export default defineComponent({
    name: 'CourseCard',
    props: {
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      },
  
      image: {
        type: [String, Object], 
         default: ''
      }
    }
  });
  </script>
  
  <style scoped>
  /* Estilos opcionales */
  .card {
    transition: transform 0.2s;
  }
  .card:hover {
    transform: translateY(-5px);
  }
  </style>