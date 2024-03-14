<template>
<div>       
    <h2 v-for="(name,index) in names" :key="name">{{index}} {{ name }}</h2>
    <h2 v-for="name in fullNames" :key="name.first">{{name.first}} {{name.last}}</h2>
    <div v-for="actor in actors" :key="actor.name">
    <h2>{{actor.name}}</h2>
    <h3 v-for="movie in actor.movies" :key="movie">{{movie}}</h3>
    </div>
    <h6 v-for="(value, key, index) in myInfo" :key="value">{{value}} ---{{key}}---- {{index}}</h6>
</div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{     
      names:["a","b","c"],
      fullNames:[
          {first: 'ahmad', last: 'malik'},
          {first: 'ahmad', last: 'malik'},
          {first: 'ahmad', last: 'malik'},
      ],
      actors:[
              {
              name:'ahmad actor',
              movies:['ali movie','hamza movie']
              }
      ],
      myInfo: {
      name: 'ahmad',
      code: 'vue 3',
      youtube: 'vishwas',
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
text-decoration:underline;
}
</style>
