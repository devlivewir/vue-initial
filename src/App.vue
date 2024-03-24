<template>
  <div>
    <template>
      <div>
        <pre>
          {{ JSON.stringify(formValues, null, 2) }}
        </pre>
      </div>
      <form action="" @submit.prevent="submitForm">
        <div>
          <label for="name">Name</label>
          <input type="text" id="name" v-model.trim.lazy="formValues.name">
        </div>

        <div>
          <label for="summary">Summary</label>
          <textarea id="summary" v-model="formValues.summary" />
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

        <div>
          <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork">
          <label for="remoteWork">Remote Work</label>
        </div>

        <div>
          <input type="number" id="age" v-model.number="formValues.age">
          <label for="remoteWork">Age</label>
        </div>
        <div>
          <button>Submit</button>
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
        'summary': '',
        'country': '',
        'jobLocation': [],
        'remoteWork': false,
        age: null,
      }
    }
  },
  methods: {
    submitForm() {
      console.log('button submitted...');
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
