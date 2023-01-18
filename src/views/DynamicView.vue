<template>
    <div>
        <h1>id : {{ id }}</h1>
        <h1>user: {{ user }}</h1>
        <h1>message: {{ message }}</h1>
    </div>
</template>
<script>
    export default{
        computed: {
            id() {
                return this.$route.params.id ;
            },
            user() {
                return this.$route.params.user ;
            },
            message() {
                return this.$route.query.message ;
            }
        }
    }
</script>