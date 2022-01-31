<template>
    <h1>Job Details Page</h1>
    <div v-if="job">
        <h2>{{ job.title }}</h2>
        <p>The Job ID is {{ id }}</p>
        <p>Details: {{ job.details }}</p>
    </div>
    <div v-else>
        <p>Loading Job details</p>
    </div>
</template>

<script>
export default {
    props: ['id', 'details'],
    data() {
        return {
            job: null
        }
    },
    mounted() {
        fetch('http://localhost:3000/jobs/' + this.id)
            .then(respose => respose.json())
            .then(data => this.job = data)
            .catch(err => console.log(err.message))
    }
}
</script>