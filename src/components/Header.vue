<template>
    <header>
        <h1>{{name}}</h1>
    </header>
</template>

<script>
    export default {
        name: 'Header',
        data()
        {
            return{
                name: "This is a Header"
            }
        }
    }
</script>

<style scoped>
    h1{
        margin-bottom: 50px;
    }
</style>