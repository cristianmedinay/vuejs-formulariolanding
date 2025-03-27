<template>
   <div>
    <AppHeader />
    
    <!-- Hero Section -->
    <section class="text-white py-5 font-img">
      <div class="container">
        <div class="row">
          <div class="col-lg-8">
            <h1 class="fw-bold mb-3">Protege tu bienestar digital</h1>
            <p class="mb-4">
              (des)CONECTA te ofrece formación gratuita para jóvenes y menores de 15 a 18 años 
              sobre la importancia de la desconexión digital y conocer los riesgos del uso 
              excesivo de la tecnología.
            </p>
            <a href="#contacto" class="btn btn-light text-danger fw-medium px-4 py-2">
              Solicita formación gratuita
            </a>
          </div>
        </div>
      </div>
    </section>
    
    <!-- What is it section -->
    <section id="que-es" class="py-5">
      <div class="container">
        <h2 class="text-danger text-center fw-bold mb-4">¿Qué es?</h2>
        <div class="row justify-content-center">
          <div class="col-lg-10 text-center">
            <p class="mb-3">
              <strong>Cursos gratuitos para jóvenes de entre 15 y 18 años para enseñarles a usar la tecnología de manera saludable, positiva y responsable</strong>, donde les ayudamos a tomar las riendas de su vida digital y crear sus propios hábitos digitales.
            </p>
            <p class="mb-4 text-secondary">
              Nuestros cursos están diseñados para que los jóvenes aprendan a gestionar su tiempo en línea, reconocer los riesgos de un uso excesivo de la tecnología y establecer una relación más saludable con sus móviles en su día a día de forma práctica y entretenida.
            </p>
            <a href="#contacto" class="btn btn-danger px-4 py-2 mb-5">
              Solicita formación gratuita
            </a>
            
            <!-- Video Section -->
            <div class="position-relative mt-4">
            <!--   <img 
                src="/placeholder.svg?height=500&width=800" 
                alt="Video thumbnail" 
                class="img-fluid rounded"
              > -->
              <button class="btn btn-light rounded-circle position-absolute top-50 start-50 translate-middle p-3 shadow">
                <i class="bi bi-play-fill fs-4 text-danger"></i>
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>
    
    <!-- What will you learn section -->
    <section id="que-aprender" class="py-5 bg-light">
      <div class="container">
        <h2 class="text-danger text-center fw-bold mb-4">¿Qué vas a aprender?</h2>
        <div class="row justify-content-center">
          <div class="col-lg-10 text-center">
            <p class="mb-5">
              En (des)CONECTA - <strong>Controla tu desconexión</strong>, organizamos <strong>cursos gratuitos para enseñar a jóvenes de 15 a 18 años sobre la desconexión digital, segura y responsable de la tecnología</strong>. Los jóvenes de esta generación son nativos digitales, pero necesitan aprender a gestionar su tiempo en línea, reconocer los riesgos y establecer una relación más saludable con sus dispositivos.
            </p>
          </div>
        </div>
        
        <div class="row g-4">
          <div class="col-md-4">
            <CourseCard 
              title="Aprenderás a gestionar diferentes dispositivos digitales" 
              description="como tu teléfono móvil, tablet o portátil, para evitar la exposición de contenido tóxico o inapropiado, y establecer límites de acceso de forma segura."
              :image=portrait
            />
          </div>
          
          <div class="col-md-4">
            <CourseCard 
              title="Descubrirás los posibles riesgos asociados con un uso excesivo de pantallas" 
              description="y aprenderás a establecer el equilibrio entre el uso de la tecnología y el disfrute de otras actividades. Podrás reflexionar sobre tus propios hábitos digitales."
              :image=frontView
            />
          </div>
          
          <div class="col-md-4">
            <CourseCard 
              title="Conocerás las herramientas de desconexión digital en tus dispositivos" 
              description="para mejorar tu bienestar digital y tu salud. Aprenderás a establecer límites de tiempo en tus redes sociales y tu teléfono personal."
              :image=girlBoyImage
            />
          </div>
        </div>
        
        <div class="text-center mt-4">
          <a href="#contacto" class="btn btn-danger px-4 py-2">
            Solicita formación gratuita
          </a>
        </div>
      </div>
    </section>
    
    <!-- Contact Form Section -->
    <ContactForm />
    
    <!-- People Image Section -->
    <section class="py-4">
      <div class="container-fluid px-0">
        <!-- <img 
          src="/placeholder.svg?height=300&width=1200" 
          alt="Group of diverse young people" 
          class="img-fluid w-100"
        > -->
      </div>
    </section>
    
    <!-- Partners Section -->
    <section class="py-5 bg-light">
      <div class="container">
        <div class="row align-items-center justify-content-center">
          <div class="col-md-5 text-center text-md-end mb-4 mb-md-0">
            <p class="small text-secondary mb-2">Una iniciativa de</p>
            <!-- <img 
              src="/placeholder.svg?height=60&width=150" 
              alt="CIBERVOLUNTARIOS logo" 
              class="img-fluid" 
              style="height: 50px; width: auto;"
            > -->
          </div>
          <div class="col-md-5 text-center text-md-start">
            <p class="small text-secondary mb-2">Con el apoyo de</p>
            <!-- <img 
              src="/placeholder.svg?height=60&width=150" 
              alt="Government logo" 
              class="img-fluid" 
              style="height: 50px; width: auto;"
            > -->
          </div>
        </div>
      </div>
    </section>
    
    <AppFooter />
  </div>
</template>

<script lang="ts">
import { defineComponent , ref} from 'vue';

import AppHeader from '../components/AppHeader.vue'
import AppFooter from '../components/AppFooter.vue'
import ContactForm from '../components/ContactForm.vue'
import CourseCard from '../components/CourseCard.vue'

import portrait from '../assets/img/portrait-woman-grabbing-head-desk-near-laptop.png'
import frontView from '../assets/img/front-view-girls-holding-smartphones.png'
import girlBoyImage from '../assets/img/girl-boy-spending-time-together-park-outside.png'
import headerHero from '../assets/img/Heade-hero.png';
export default defineComponent({
    name: 'Homeview',
    data() {
        return {
    };
    },
    props: {},

    components: {AppHeader,
    AppFooter,
    ContactForm,
    CourseCard},

    setup(props, { context }) {

       

    const heroStyle = ref({
    backgroundImage: `url(${headerHero})`,
  
    });
        return{
            girlBoyImage,
            frontView,
            portrait,
            
            heroStyle
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
.home-page section {
  padding: 4rem 0;
}
.font-img {
  color: white;
  padding: 4rem 0;
  background-image: v-bind('heroStyle.backgroundImage');
  background-size: cover; 
  background-position: center;
  background-repeat: no-repeat;
  
  position: relative;
  
  
  &::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
   
    z-index: 0;
  }

  .container {
    position: relative;
    z-index: 1;
  }
}
.bg-danger {
  background: linear-gradient(135deg, #dc3545, #c82333);
}
</style>