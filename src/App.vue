<template>
<div>
  <h1>Hello World</h1>
  <UserComp />
</div>
</template>
<script>
//import MyNewComp from './components/MyNewComp'
//import BookComp from './components/BookComp'
//import ProductComp from './components/ProductComp'
//import DirectiveComp from './components/DirectiveComp'
//import CustomDir2 from './components/customdir2.js'
import UserComp from './components/UserComp'
export default {
  components: {
    //MyNewComp,
    //BookComp,
    //ProductComp,
    //DirectiveComp,
   UserComp
,
   
  },
  //directives:{colorStyle : CustomDir2},
  data() {
    return {
      products: [
        {"name":"laptop1", "price":1100000},
        {"name":"laptop2", "price":1200000},
        {"name":"laptop3", "price":1300000},
        {"name":"laptop4", "price":1400000}
      ]
    }
  },
  
}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
