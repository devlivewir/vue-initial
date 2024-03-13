<template>
<div>
  <div>{{greating}} {{message}}</div>
  <div> {{name}} </div>
  <div v-text="name"></div>
  <div v-html="type"></div>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
  <h2 class="underline">under line Text</h2>
  <h2 v-bind="status">Status</h2>
  <h2 v-bind="isPromoted && 'promoted'">Promoted Movie</h2>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      greating:"Hello",
      name:"Maria",
      message:" you are looking so beautifull",
      type:"<b>paragraph type is text</b>",
      headingId: 'heading',
      isDisabled: false,
      status: 'danger',
      isPromoted: true
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
