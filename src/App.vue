<template>
<div>
  <div>{{greating}} {{message}}</div>
  <div> {{name}} </div>
  <div v-text="name"></div>
  <div v-html="type"></div>
  <h2 :id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
  <h2 class="underline">under line Text</h2>
  <h2 v-bind="status">Status</h2>
  <h2 v-bind="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 v-bind="iaSold ? 'sold-out':'new'">SoldOut? Movie</h2>
  
  <h2 v-bind:class="{
  promoted: isPromoted,

  }">object key value pairs</h2>

  <h2 v-bind:style="{
        color: 'orange',
        padding: '20px',
        }">sytle in v binding</h2>

        <h2  v-bind:style="[baseStyleObject,successStyleObject]">Success</h2>
        
        
        <h2 v-if="num===0">The Number is  Zero</h2>
        <h2 v-else>The Number Is not Zero</h2>
        <div v-if="display">
        <h2>Ahmad</h2>
        <h2>Ahmad 1</h2>
        <h2>Ahmad 2</h2>
        </div>
        
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
      isPromoted: true,
      isSold: true,
      successStyleObject:{
          color:'darked',
          backgroundColor: 'green',
          border: '1px solid dark Gray',
      },
      baseStyleObject:{
      fontZise: '50px',
      padding: '20px',
      },
      num:5,
      display:true,
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
