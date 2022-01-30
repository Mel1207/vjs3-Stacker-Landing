<template>
  <div class="jobs">
    <h1>Job List</h1>
    <div v-for="job in jobs" :key="job.id" class="job">
      <router-link :to="{ name: 'JobDetails', params: {id: job.id, details: job.details}}">
        <h2>{{ job.title }}</h2>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        {title: 'Frontend Developer', id: 1, details: 'lorem'},
        {title: 'Backend Developer', id: 2, details: 'lorem ipsum'},
        {title: 'UI-UX Designer', id: 3, details: 'lorem dolor'},
      ]
    }
  }
}
</script>
