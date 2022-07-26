<template>
<User> </User>
 <div>
  <h1>Home Component</h1>
  
  <!-- <Product/> -->
 </div>
 <ChildHome></ChildHome>
</template>

<script>
import User from './User.vue'
// import Product from './Product.vue'
// import childHome from './childHome.vue'
import ChildHome from './childHome.vue'

export default {
    name: "App",
    // components: {
    //     childHome
    //     // User,
    //     // Product
    // },
    components: { ChildHome, User }
};
</script>
<style >
div{
 background-color: gray;
    height: 100vh;
    width: 100vw;    
} 
</style>