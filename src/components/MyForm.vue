<template><div>
  <input type="text" v-model="myName">
  <input type="text" v-model="age">
  <br> Name : {{myName}}
  <br> Age : {{age}}
  <input type="radio" id="Male" value="Male" v-model="gender">Male
  <input type="radio" id="female" value="female" v-model="gender">Female
  <button v-on:click="displayData()">Click to Save the data</button>
  </div>
</template>

<script>
export default {
    name: 'FormData',
    data() {
        return {
            myName : '',
            age : '',
            gender : ''
        }
    },
    methods: {
        displayData() {
            console.log(this.myName);
            console.log(this.age)
            console.log(this.gender)
        }
    },
}
</script>

<style>

</style>
