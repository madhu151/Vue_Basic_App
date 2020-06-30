<template>
    <div>
        <h1>Book Shop Name is {{bookShopNmae}}</h1>
        <label for="bookName">Book Name </label>{{Book.name}}<br>
        <label for="bookPrice">Book Price</label>{{Book.price}}<br>

    </div>
</template>

<script>
export default {
    name: "BookComp",
    data() {
        return {
            bookShopNmae: "IRC"
        }
    },
    props: {
        Book: {
            name: String,
            price:Number 
        },
    },

}
</script>

<style scoped>


    h1{
        color: greenyellow
    }
</style>
