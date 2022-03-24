<template>
  <div class="container mx-auto p-4">
    <!-- <div>Hola</div>
    <input type="number" v-model.number="max1" class="border" />
    <Counter :max="max1" />
    <Counter :max="10" />
    <Counter :max="20" /> -->
    <Bank />
  </div>
</template>
<script>
import Bank from "./components/Bank.vue";
// 1: importar el component
// import HelloWorld from "./components/Bank.vue";

// 2. declarar components
export default {
  components: {
    Bank,
  },
};
</script>

<style></style>
