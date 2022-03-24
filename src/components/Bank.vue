<template>
  <h1>Bank</h1>
  <div>Income: {{ income }}€</div>
  <div>Outcome: {{ outcome }}€</div>
  <div>Balance: {{ balance }}€</div>

  <input type="text" class="border" v-model="name" placeholder="Name" />

  <input type="number" class="border" v-model="amount" placeholder="Amount" />

  <button class="bg-teal-500 text-white px-2 rounded" @click="addItem">
    Add
  </button>

  <ul>
    <li v-for="(item, i) in items" :key="i">
      {{ item.name }} {{ item.amount }}€
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      amount: 0,
      items: [],
    };
  },
  computed: {
    income() {
      return this.items
        .filter((item) => item.amount > 0)
        .reduce((acc, item) => acc + item.amount, 0);
    },
    outcome() {
      return this.items
        .filter((item) => item.amount < 0)
        .reduce((acc, item) => acc + item.amount, 0);
    },
    balance() {
      return this.income + this.outcome;
    },
  },
  methods: {
    addItem() {
      this.items.push({
        name: this.name,
        amount: this.amount,
      });
    },
  },
};
</script>
