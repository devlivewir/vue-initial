<template>
  <div>
    <div v-for="name in names" :key="name">
      <h2>{{ name }}</h2>
      <input placeholder="last name" />
      <hr>
    </div>

    <button @click="shuffle">shuffle</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{     
      names:["a","b","c"],
      
    }
  },
  methods: {
    shuffle(){
    console.log(this.names);
    //this.names = _.shuffle(this.names);
    }
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
text-decoration:underline;
}
</style>
