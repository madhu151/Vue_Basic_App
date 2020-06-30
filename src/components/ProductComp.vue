<template>
  <div>
      <h2>List of Products</h2>
      <ul>
          <li v-for="p in products" :key="p.price">
              <span>{{p.name}}</span> -- 
              <span>{{p.price}}</span>
          </li>
      </ul>
      <h3>{{this.count}}</h3><button v-on:click="incrementData">Add 1</button>
        <h4>{{getMyName}}</h4>
        <h5>Increment count with Computed : {{incrementCount}}</h5>
  </div>
</template>

<script>
export default {
    name:"ProductComp",
    props: 
       ['products'] 
        
    ,
    data() {
        return {
            count: 0,
            myName : ""
        }
    },
    
    methods: {
        incrementData() {
            return this.count++
        }
    },
    computed: {
        getMyName() {
            return this.myName + " Snigdha " 
        },
        incrementCount(){
            return this.count + 1;
        }
    },
}

</script>

<style>

</style>
