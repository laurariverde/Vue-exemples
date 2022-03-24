<template>
  <h1>Bank</h1>
  <div>Income:{{ income }}€</div>
  <div>Income:{{ outcome }}€</div>
  <div>Income:{{ balance }}€</div>

  <imput type="text" class="border" v-model="name" placeholder="Name" />
  <imput type="number" class="border" v-model="amount" placeholder="Amount" />
  <button class="bg-teal-500 text-white px-2 rounded" key="" @clik="addItem">
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
      outcome: -30,
      name: "",
      amount: 0,
      items: [],
    };
  },
  computed: {
    income() {
      return this.items
        .filter((item) => acc + item.amount > 0)
        .reduce((acc, item) => acc + item < 0);
    },
    balance() {
      return this.icome + this.outcome;
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
