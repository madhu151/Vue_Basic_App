<template>
    <div>
        <h1>My Second Component</h1>
        <h3>Component Design by {{myname}}</h3>
        <h4>Age is {{age}}</h4>
    </div>
</template>

<script>

export default {
     name : "MyNewComp",
    props: {
        myname : {
            type: String,
            required: true
            
        },
        age :{
            type: String,
            validator: function(value){
                let myValue = parseInt(value)
                return myValue >=18 && myValue <= 50
            }
        },
        gender: {
            type: String,
            validator: function(value){
                return ['male', 'female'].includes(value)
            }
        }
    }
}
</script>

<style>

</style>

