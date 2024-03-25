<template>
  <div>
    <template>
      <h2>FullName - {{ firstName }} {{ lastName }}</h2>
      <h2>Computed FullName - {{ FullName }}</h2>
      <h2>Total -{{ items.reduce((total, curr) => (total = total + curr.price), 0) }} </h2>
      <h2>with total computed method - {{ total }} </h2>
      <button @click="items.push({ id: 4, title: 'keyBoard', price: 50 })">Add item</button>
      <h2>Get Total  Method -{{ getTotal() }}</h2>
      <input type="text" v-model="country">
    </template>
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
      country:''
    }
  },
  methods: {
    getTotal() {
      console.log('get Total Method');
      return this.items.reduce((total, curr) => (total = total + curr.price), 0)
    }
  },
  computed: {
    FullName() {
      return `${this.firstName} ${this.lastName}`
    },
    total() {
      console.log('get total property');
      return this.items.reduce((total, curr) => (total = total + curr.price), 0)
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
