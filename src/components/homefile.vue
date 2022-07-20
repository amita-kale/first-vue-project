<template>
 
 <div>
  <!-- <h1 v-if="show">show true then else text printed "Hello"</h1>
  <h1 v-else>show false then else text printed "Hello"</h1> -->
  <h2>{{demo}}</h2>
  
  <!-- <button v-on:click="hello('submit click')">Submit</button>  -->
  <br>
  <button v-on:click="show=!show">Show hide div</button>

  <div class="div" v-if="show">"I am amita"</div>
  
 </div>
</template>

<script>
export default {
  name:"home-file",
  data(){
    return {show:true}
  },
  props: {
    //msg: String,
    demo:String,
    
  },
  methods:{
    // hello(){
    //   // console.log("hi submit clicked");
    //   return{show:true}

    // }
    //parameterised fun
    //  hello(data){
    //   alert(data);
    // }
  }
}
</script>
<style>
.div{
  background-color:aqua;
  height: 20%;
  width: 20%;
  color: red;
  align-items: center;
 
}
</style>
