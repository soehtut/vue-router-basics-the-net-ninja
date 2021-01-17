<template>
    <!-- <div>Job ID is {{ $route.params.id }}</div> -->
    <!-- <div>Job ID is {{ id }}</div> -->
    <div v-if="job">
        <h1>{{ job.title }}</h1>
        <p>{{ job.details }}</p>
    </div>
    <div v-else>
        Loading job details....
    </div>
</template>

<script>
export default {
    props: ['id'],
    data() {
        return {
            // id: this.$route.params.id
            job: null
        }
    },
    mounted() {
        fetch('http://localhost:3000/jobs/' + this.id)
        .then(res => res.json())
        .then(data => this.job = data)
        .catch(err => console.log(err.message))
    }
}
</script>
