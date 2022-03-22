<template>
  <div class="bg-gray-100 rounded shadow mb-4">
    <h1>{{ message }}</h1>
    <input type="text" v-model="message" class="border" />
  </div>
</template>
<script>
export default {
  data() {
    return {
      message: "",
    };
  }
  };
</script>