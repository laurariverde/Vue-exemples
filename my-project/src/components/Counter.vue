<template>
  <div>The count is: {{ count }}</div>
  <button class="boder px-4 py-2 rounder" @click="count++">+1</button>
</template>

<script>
export default {
  data() {
    return {
      cont: 0,
    };
  },
};
</script>

<style></style>
