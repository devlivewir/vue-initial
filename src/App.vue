<template>
  <div>
    <Greet name="bruce" heroName="supper" />
    <Greet name="alli" heroName="dupper" />
    <Greet name="ahi" heroName="happer" />
    <Greet :name="name" :heroName="channel" />

    <Artical :likes="50" :isBoolean="true" />
    <ComponentC />

  </div>

</template>

<script>
import Greet from './components/Greets.vue'
import Artical from './components/Artical.vue'
import ComponentC from './components/ComponentC.vue'
export default {
  name: 'App',
  components: {
    Greet,
    Artical,
    ComponentC
  },
  data() {
    return {
      name: 'Ali Name',
      channel: 'ahmad video'
    }
  },
  provide() {
    return {
      username: this.name
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
