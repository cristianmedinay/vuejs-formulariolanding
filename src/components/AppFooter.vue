<template>
  <footer class="bg-danger text-white py-5">
    <div class="container">
      <div class="row gy-4">
        <div class="col-md-4">
          <!-- <img src="/placeholder.svg?height=40&width=150" alt="(des)CONECTA logo" class="img-fluid mb-3" style="height: 40px; width: auto;" /> -->
          <img :src=logodesconectaFooter alt="(des)CONECTA logo" class="img-fluid mb-3" style="height: 100px; width: auto;" />
          <div class="small">
            <p class="mb-1">Calle</p>
            <p class="mb-1">Ciudad, CP</p>
            <p class="mb-0">Solicita información gratuita</p>
          </div>
        </div>
        <div class="col-md-4">
          <h5 class="fw-bold mb-3">Contáctanos</h5>
          <div class="small">
            <p class="mb-1">+34 XXX XX XX XX</p>
            <p class="mb-0">info@desconecta.org</p>
          </div>
        </div>
        <div class="col-md-4">
          <h5 class="fw-bold mb-3">Conéctate con nosotros</h5>
          <div class="d-flex gap-2">
            <a href="#" class="btn btn-sm btn-outline-light rounded-circle">
              <i class="bi bi-facebook"></i>
            </a>
            <a href="#" class="btn btn-sm btn-outline-light rounded-circle">
              <i class="bi bi-twitter"></i>
            </a>
            <a href="#" class="btn btn-sm btn-outline-light rounded-circle">
              <i class="bi bi-instagram"></i>
            </a>
            <a href="#" class="btn btn-sm btn-outline-light rounded-circle">
              <i class="bi bi-linkedin"></i>
            </a>
          </div>
        </div>
      </div>
      <div class="border-top border-white border-opacity-25 mt-4 pt-4">
        <p class="small mb-0">© 2025 (des)CONECTA | Todos los derechos reservados | Aviso legal | Política de privacidad | Cookies</p>
      </div>
    </div>
  </footer>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import logodesconectaFooter from '../assets/img/LOGO DESCONECTA-OK-BLANCO.png';
export default defineComponent({
    name: 'AppFooter',
    data() {
        return {};
    },
    props: {},

    components: {},

    setup(props, { context }) {

        return{
            logodesconectaFooter
        }

    },

    mounted() {},

    methods: {},

    computed: {},

    watch: {},

    directives: {},

    filters: {}
});
</script>

<style lang="scss" scoped>
.btn-outline-light {
  width: 32px;
  height: 32px;
  padding: 0;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>