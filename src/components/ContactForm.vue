<template>
    <section id="contacto" class="py-5">
      <div class="container">
        <h2 class="text-danger text-center fw-bold mb-4">Solicita formación gratuita</h2>
        
        <div class="row justify-content-center">
          <div class="col-lg-8">
            <form @submit.prevent="submitForm" class="needs-validation" novalidate>
              <div class="row g-3 mb-3">
                <div class="col-md-6">
                  <input 
                    type="text" 
                    class="form-control" 
                    placeholder="Nombre" 
                    v-model="formData.nombre"
                    required
                  >
                </div>
                <div class="col-md-6">
                  <input 
                    type="text" 
                    class="form-control" 
                    placeholder="Apellidos" 
                    v-model="formData.apellidos"
                    required
                  >
                </div>
              </div>
              
              <div class="row g-3 mb-3">
                <div class="col-md-6">
                  <input 
                    type="email" 
                    class="form-control" 
                    placeholder="Email" 
                    v-model="formData.email"
                    required
                  >
                </div>
                <div class="col-md-6">
                  <input 
                    type="tel" 
                    class="form-control" 
                    placeholder="Teléfono" 
                    v-model="formData.telefono"
                  >
                </div>
              </div>
              
              <div class="mb-3">
                <select class="form-select" v-model="formData.provincia" required>
                  <option value="" disabled selected>Provincia</option>
                  <option value="madrid">Madrid</option>
                  <option value="barcelona">Barcelona</option>
                  <option value="valencia">Valencia</option>
                  <option value="sevilla">Sevilla</option>
                  <option value="otras">Otras</option>
                </select>
              </div>
              
              <div class="mb-3">
                <label class="form-label small text-secondary">Centro o ubicación:</label>
                <input 
                  type="text" 
                  class="form-control" 
                  placeholder="Ej: IES Ramiro de Maeztu, centro cultural..." 
                  v-model="formData.centro"
                >
              </div>
              
              <div class="mb-3 form-check">
                <input 
                  type="checkbox" 
                  class="form-check-input" 
                  id="comunicaciones" 
                  v-model="formData.comunicaciones"
                >
                <label class="form-check-label small" for="comunicaciones">
                  Acepto recibir comunicaciones de (des)CONECTA EDUCACIÓN
                </label>
              </div>
              
              <div class="small text-secondary mb-4">
                Al enviar este formulario, aceptas nuestra 
                <a href="#" class="text-danger">Política de Privacidad</a> y los 
                <a href="#" class="text-danger">Términos de Condiciones</a> 
                <span class="text-danger">*</span>
              </div>
              
              <button type="submit" class="btn btn-danger w-100 py-2">Solicitar</button>
            </form>
            
            <!-- Tabla de datos enviados -->
            <div v-if="submittedData.length > 0" class="mt-5">
              <h3 class="text-danger fw-bold mb-3">Solicitudes enviadas</h3>
              <div class="table-responsive">
                <table class="table table-striped table-hover">
                  <thead class="table-danger">
                    <tr>
                      <th>Nombre</th>
                      <th>Apellidos</th>
                      <th>Email</th>
                      <th>Teléfono</th>
                      <th>Provincia</th>
                      <th>Centro</th>
                      <th>Comunicaciones</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr v-for="(item, index) in submittedData" :key="index">
                      <td>{{ item.nombre }}</td>
                      <td>{{ item.apellidos }}</td>
                      <td>{{ item.email }}</td>
                      <td>{{ item.telefono || '-' }}</td>
                      <td>{{ item.provincia }}</td>
                      <td>{{ item.centro || '-' }}</td>
                      <td>
                        <span v-if="item.comunicaciones" class="badge bg-success">Sí</span>
                        <span v-else class="badge bg-secondary">No</span>
                      </td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
</template>
  
  <script lang="ts">
  import { defineComponent } from 'vue';
  import { FormData } from '../interface/interfaces';
  
  export default defineComponent({
    name: 'ContactForm',
    components: {},
    data() {
      return {
        formData: {
          nombre: '',
          apellidos: '',
          email: '',
          telefono: '',
          provincia: '',
          centro: '',
          comunicaciones: false
        } as FormData,
        submittedData: [] as FormData[]
      }
    },
    props: {},
  
    setup(props, { context }) {},
  
    mounted() {},
  
    methods: {
      submitForm() {
        // Form validation
        if (!this.validateForm()) {
          return;
        }
        
        // Add the current form data to the submitted data array
        this.submittedData.push({...this.formData});
        
        // Here you would typically send the form data to a server
        console.log('Form submitted:', this.formData);
        
        // Reset form
        this.resetForm();
      },
      validateForm() {
        // Basic validation
        if (!this.formData.nombre || !this.formData.apellidos || !this.formData.email || !this.formData.provincia) {
          alert('Por favor, complete todos los campos obligatorios');
          return false;
        }
        
        // Email validation
        const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        if (!emailRegex.test(this.formData.email)) {
          alert('Por favor, introduzca un email válido');
          return false;
        }
        
        return true;
      },
      resetForm() {
        this.formData = {
          nombre: '',
          apellidos: '',
          email: '',
          telefono: '',
          provincia: '',
          centro: '',
          comunicaciones: false
        };
      }
    },
  
    computed: {},
  
    watch: {},
  
    directives: {},
  
    filters: {}
  });
  </script>
  
  <style lang="scss" scoped>
  .table-responsive {
    max-height: 400px;
    overflow-y: auto;
  }
  
  .badge {
    font-weight: normal;
    padding: 0.35em 0.65em;
  }
  
  .table-danger {
    background-color: rgba(229, 62, 62, 0.1);
  }
  
  .table-danger th {
    color: #e53e3e;
    font-weight: 600;
    border-bottom: none;
  }
  
  .table-striped > tbody > tr:nth-of-type(odd) {
    background-color: rgba(0, 0, 0, 0.02);
  }
  
  .table-hover > tbody > tr:hover {
    background-color: rgba(229, 62, 62, 0.05);
  }
  </style>