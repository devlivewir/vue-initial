<template>
  <div>
    <h2>FullName - {{ firstName }} {{ lastName }}</h2>
    <h2>Computed FullName - {{ FullName }}</h2>
    <h2>Total - {{ getTotal() }}</h2>
    <h2>with total computed method - {{ total }}</h2>
    <button @click="addItem">Add item</button>
    <h2>Get Total Method - {{ getTotal() }}</h2>
    <input type="text" v-model="country">
    <div v-for="item in items" :key="item.id">
      <h2>{{ item.title }} - {{ item.price }}</h2>
    </div>

    <h2 v-for="item in expensiveItems" :key="item.id">
      {{ item.title }}
      -
      {{ item.price }}
    </h2>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      firstName: "Hafiz",
      lastName: "Ahmad",
      items: [
        {
          id: 1,
          title: 'TV',
          price: 200
        },
        {
          id: 2,
          title: 'Watch',
          price: 150
        },
        {
          id: 3,
          title: 'Screen',
          price: 170
        },
      ],
      country: ''
    }
  },
  methods: {
    addItem() {
      this.items.push({ id: 4, title: 'keyBoard', price: 50 });
    },
    getTotal() {
      return this.items.reduce((total, curr) => total + curr.price, 0);
    }
  },
  computed: {
    FullName() {
      return `${this.firstName} ${this.lastName}`;
    },
    total() {
      return this.getTotal();
    },
    expensiveItems() {
      return this.items.filter(item => item.price > 40);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.underline {
  text-decoration: underline;
}
</style>
