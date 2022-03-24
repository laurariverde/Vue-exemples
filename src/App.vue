<template>
  <div class="container mx-auto p-4">
    <div>Hola</div>
    <!-- 3. utilitzar el component al template -->
    <input type="number" v-model.number="max1" class="border" />
    <Counter :max="max1" />
    <Counter :max="10" />
    <Counter :max="20" />
  </div>
</template>
<script>
// 1: importar el component
import HelloWorld from "./components/HelloWorld.vue";
import Counter from "./components/Counter.vue";
export default {
  // 2: registrar el component
  components: {
    HelloWorld,
    Counter,
  },
  data() {
    return {
      max1: 10,
    };
  },
};
</script>

<style></style>
