<template>
  <div class="bg-gray-100 mb-4 p-2 rounded shadow">
    <div>
      The count is:
      <span
        :class="{
          'text-red-600': count === max,
          'text-orange-400': count >= max - 3 && count < max,
          'text-green-600': count < max - 3,
        }"
        >{{ count }}</span
      >
    </div>
    <button class="border px-4 py-2 rounded bg-white" @click="decrease">
      -1
    </button>
    <button
      class="border px-4 py-2 rounded bg-white"
      :class="{ 'text-gray-300': count === max }"
      :disabled="count === max"
      @click="increase"
    >
      +1
    </button>
  </div>
</template>
<script>
export default {
  props: ["max"],
  data: () => ({
    count: 0,
  }),
  methods: {
    decrease() {
      if (this.count > 0) this.count--;
    },
    increase() {
      if (this.count < this.max) this.count++;
    },
  },
};
</script>
