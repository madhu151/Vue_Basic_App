<template>
    <div>
        <h1>Users Data</h1>
        <button v-on:click="getUsers">Get Users</button>
    </div>
</template>

<script>
export default {
    name: 'UserComp',
    data() {
        return {
            users : []
        }
    },
    methods: {
       
        getUsers() {
            alert("method call")
            let body = {

            }
           this.$http.post("https://jsonplaceholder.typicode.com/users", body)
            .then(function(response) {
                console.log(response);
            })
            .catch(error => {
                console.log(error);
            })
        }
    },
}
</script>
<style>

</style>
