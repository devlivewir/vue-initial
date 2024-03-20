<template>
  <div>
    <template>
      <div>
        <pre>
          {{ JSON.stringify(formValues, null, 2) }}
        </pre>
      </div>
      <form action="">
        <div>
          <label for="name">Name</label>
          <input type="text" id="name" v-model="formValues.name">
        </div>

        <div>
          <label for="summary">Summary</label>
          <textarea id="summary" v-model="formValues.summary"/>
        </div>

        <div>
          <label for="country">Country</label>
          <select name="" id="country" v-model="formValues.country">
            <option value="">Select Country</option>
            <option value="Pakistan">Pakistan</option>
            <option value="India">India</option>
          </select>
        </div>

        <div>
          <label for="job-location">Job Location</label>
          <select name="" id="job-location" multiple v-model="formValues.jobLocation">
            <option value="">Select Country</option>
            <option value="Pakistan">Pakistan</option>
            <option value="India">India</option>
          </select>
        </div>
      </form>
    </template>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      formValues: {
        name: '',
        'summary':'',
        'country':'',
        'jobLocation':[]
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
