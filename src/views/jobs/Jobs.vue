<template>
    <h1>Jobs</h1>
    <div v-for="job in jobs" :key="job.id">{{ job.title }}</div>
</template>

<script>
export default {
    data() {
        return {
            jobs: [
                {id: 1, title: 'Web Designer'},
                {id: 2, title: 'Web Developer'},
                {id: 3, title: 'React Native Developer'}
            ]
        }
    }
}
</script>

