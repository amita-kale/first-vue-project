<template>
 
 <div>
  <h1 v-if="show">show true then else text printed "Hello"</h1>
  <h1 v-else>show false then else text printed "Hello"</h1>
  <h2>{{demo}}</h2>
  <button v-on:click="hello('submit click')">Submit</button>
  
 </div>
</template>

<script>
export default {
  name:"home-file",
  props: {
    //msg: String,
    demo:String
  },
  methods:{
    hello(){
      // console.log("hi submit clicked");
      return{show:false}

    }
    //parameterised fun
    //  hello(data){
    //   alert(data);
    // }
  }
}
</script>
