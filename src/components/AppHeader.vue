<template>
 <header class="bg-dark text-white py-3">
    <div class="container">
      <div class="d-flex justify-content-between align-items-center">
        <div class="logo">
          <img src="../assets/img/LOGO DESCONECTA-BLANCO Y ROJO.png" alt="(des)CONECTA logo" height="40" class="img-fluid" />
       
        </div>
        <nav class="d-none d-md-flex">
          <ul class="list-unstyled d-flex mb-0">
            <li class="me-4"><a href="#que-es" class="text-white text-decoration-none">Qué es</a></li>
            <li class="me-4"><a href="#que-aprender" class="text-white text-decoration-none">Qué vas a aprender</a></li>
            <li><a href="#contacto" class="text-white text-decoration-none">Solicita formación</a></li>
          </ul>
        </nav>
        <button class="btn btn-sm d-md-none text-white" type="button" data-bs-toggle="collapse" data-bs-target="#mobileMenu">
          <i class="bi bi-list fs-4"></i>
        </button>
      </div>
    </div>
    <div class="collapse d-md-none" id="mobileMenu">
      <div class="container py-2">
        <ul class="list-unstyled">
          <li class="mb-2"><a href="#que-es" class="text-white text-decoration-none">Qué es</a></li>
          <li class="mb-2"><a href="#que-aprender" class="text-white text-decoration-none">Qué vas a aprender</a></li>
          <li><a href="#contacto" class="text-white text-decoration-none">Solicita formación</a></li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
    name: 'AppHeader',
    data() {
        return {};
    },
    props: {},

    components: {},

    setup(props, { context }) {},

    mounted() {},

    methods: {},

    computed: {},

    watch: {},

    directives: {},

    filters: {}
});
</script>

<style lang="scss" scoped>
.logo img {
  height: 40px;
  width: auto;
}
</style>