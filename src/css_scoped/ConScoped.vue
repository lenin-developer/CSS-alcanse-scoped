<script setup lang="ts">
import ComponenteTest from '../components/ComponenteTest.vue';
import ComponentePTest from '../components/ComponentePTest.vue';
</script>

<template>
  <ComponenteTest class="example2" />
  <ComponentePTest />
</template>

<style scoped>
.example2 :deep(.example) {
  background: pink;
}

.example-p {
  background: blue;
  border: none;
}
</style>
