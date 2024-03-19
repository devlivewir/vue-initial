<template>
  <div>
    <template>
      {{ 2 + 3 + 6 }}
      <h2>hheha</h2>
      <h6>Add method = {{ add(10, 20, 30) }}</h6>
      <h6>Add method = {{ add(40, 50, 60) }}</h6>
      <h6>Add method = {{ add(70, 80, 90) }}</h6>
      <h6>Add * {{ mult(300) }}</h6>
    </template>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      baseMultiplyer: 5,

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
