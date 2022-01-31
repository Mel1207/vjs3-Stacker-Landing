<template>
  <div class="jobs">
    <h1>Job List</h1>
    <div v-for="job in jobs" :key="job.id" class="job">
      <router-link :to="{ name: 'JobDetails', params: {id: job.id}}">
        <h2>{{ job.title }}</h2>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: []
    }
  },
  mounted() {
    fetch('http://localhost:3000/jobs')
      .then(respose => respose.json())
      .then(data => this.jobs = data)
      .catch(err => console.log(err.message))
  }
}
</script>
