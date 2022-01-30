<template>
  <div class="jobs">
    <h1>Job List</h1>
    <div v-for="job in jobs" :key="job.id">
      <h2>{{ job.title }}</h2>
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
