<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue';
import SinScoped from './css_scoped/SinScoped.vue';
import ConScoped from './css_scoped/ConScoped.vue';
import SlottedPseudoCalse from './css_scoped/SlottedPseudoCalse.vue';
</script>

<template>
  <HelloWorld />
  <p>
    Nota muy importente con un stylo que no tenga el scoped y que una de sus
    compoentes hijos tengas el mismo nombre de clase o por etiqueta ya afecta a
    todos los hijos
  </p>
  <p>
    algo similar pasa si mi componente padre tiene scoped y tiene una clase con
    el mismo nombre que un componene hijo igual lo afecta siempre y cuando el
    hijo solo tenga un unico elemento (parrafo con fondo azul)
  </p>
  <p>
    por lo que veo siempre siempre siempre se debe de utilizar el scoped y si
    quiere pasar estilos del padre al hijo hacerlo explicito con las pseudo
    clases :deep y :slotted
  </p>
  <h2>sin scoped</h2>
  <SinScoped />
  <h2>con scoped</h2>
  <ConScoped />
  <h2>:slott</h2>
  <SlottedPseudoCalse />
</template>

<style scoped>
:global(p) {
  border: 3px solid red;
}
</style>
