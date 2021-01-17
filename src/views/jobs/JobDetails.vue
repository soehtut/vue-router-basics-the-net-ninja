<template>
    <h1>Job Details</h1>
    <!-- <div>Job ID is {{ $route.params.id }}</div> -->
    <div>Job ID is {{ id }}</div>
</template>

<script>
export default {
    data() {
        return {
            id: this.$route.params.id
        }
    }
}
</script>
