<script>
    export default {
        props: {
            title: String,
        },
        computed: {
            transform(){
                return this.title.toLowerCase()
            },
        },
    }
</script>


<template>
    <h4>{{ title }}</h4>
    <h4>{{ transform }}</h4>
</template>

<style></style>