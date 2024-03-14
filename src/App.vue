<template>
<div>
        <div v-if="display">
            <h2>Ahmad</h2>
            <h2>Ahmad 1</h2>
            <h2>Ahmad 2</h2>
        </div>
        <h2 v-show="showElement">v show Element</h2>
        
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{     
      num:5,
      display:true,
      showElement: false,
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
text-decoration:underline;
}
</style>
