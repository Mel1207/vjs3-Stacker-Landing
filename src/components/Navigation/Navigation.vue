<template>
    <div id="nav">
        <router-link to="/">Home</router-link> |
        <router-link :to="{ name: 'About'}">About</router-link> |
        <router-link :to="{ name: 'Jobs'}">Jobs</router-link>
    </div>
</template>

<script>
export default {
}
</script>