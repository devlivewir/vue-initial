<template>
  <div>
    <template>
      {{ 2 + 3 + 6 }}
      <h2>hheha</h2>
      <h6>Add method = {{ add(10, 20, 30) }}</h6>
      <h6>Add method = {{ add(40, 50, 60) }}</h6>
      <h6>Add method = {{ add(70, 80, 90) }}</h6>
      <h6>Add * {{ mult(300) }}</h6>
      <div>
        <button v-on:click="name = 'Bat Man'">Change the Name</button>
      </div>
      <h2>{{ count }}</h2>

      <button v-on:click="count +=  1">Increment</button>
      <button v-on:click="count -=  1">Decrement</button>
    </template>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      baseMultiplyer: 5,
      name: "alic",
      count: 0,

    }
  },
  methods: {
    shuffle() {
      // console.log(this.names);
      //this.names = _.shuffle(this.names);
    },
    add(a, b, c) {
      return a + b + c
    },
    mult(num) {
      return num * this.baseMultiplyer
    },
  },

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
