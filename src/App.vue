<template>
  <div>
    <h2>Volum tracker (0 20)</h2>
    <h3>Current Volume => {{ volume }}</h3>
    <button @click="volume += 2">Increase</button>
    <button @click="volume -= 2">Decrease</button>

  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      volume: 0
    }
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert('the value is heigh');
      }
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
