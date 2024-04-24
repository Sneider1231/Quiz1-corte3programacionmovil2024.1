<template>
  <img :src="imageUrl" :alt="altText" :id="id" :class="imageClass" :style="imageStyle">
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  props: {
    id: {
      type: String,
      required: true
    },
    imageUrl: {
      type: String,
      required: true
    },
    altText: {
      type: String,
      required: true
    },
    imageClass: String,
    imageStyle: Object
  }
});
</script>

<style scoped>
  /* Estilos específicos del componente */
</style>
