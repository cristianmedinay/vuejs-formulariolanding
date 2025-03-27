<template>
 <div class="card h-100 border-0 shadow-sm">
    <div class="card-body p-4">
      <div class="text-center mb-3">
        <div class="bg-danger bg-opacity-10 rounded-circle p-3 d-inline-flex mb-3">
          <img :src="icon" :alt="title" class="img-fluid" width="40" height="40">
        </div>
        <h3 class="card-title fw-bold fs-5">{{ title }}</h3>
      </div>
      <p class="card-text text-center text-secondary">{{ description }}</p>
      <div class="mt-4">
        <img :src="image" :alt="title" class="img-fluid rounded">
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
    name: 'CourseCard',
    data() {
        return {};
    },
    props: {
        title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    icon: {
      type: String,
     /*  default: '/placeholder.svg?height=40&width=40' */
    },
    image: {
      type: String,
     /*  default: '/placeholder.svg?height=200&width=300' */
    }
  },

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

</style>