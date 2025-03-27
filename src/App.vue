<template>
 <div >
  <HomeView />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HomeView from './views/Homeview.vue'
export default defineComponent({
    name: 'App',
  
    props: {},

    components: {
      HomeView
    },

    setup(props, { context }) {},

 
});
</script>

<style lang="scss" scoped>

</style>