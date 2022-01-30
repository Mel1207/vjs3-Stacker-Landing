<template>
    <h1>Job Details Page</h1>
    <p>The Job ID is {{ id }}</p>
    <p>Details: {{ details }}</p>
</template>

<script>
export default {
    props: ['id', 'details'],
    // data() {
    //     return {
    //         id: this.$route.params.id
    //     }
    // }
}
</script>