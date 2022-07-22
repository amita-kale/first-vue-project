<template>
 
 <div>
  <h1 v-if="show">show true then if text printed "Hello"</h1>
  <h1 v-else>show false then else text printed "Hello"</h1>
  <h2>{{demo}}</h2>
  
  <button v-on:click="hello">Submit</button> 
  <br>
  <button v-on:click="show1=!show1">Show hide div</button>

  <div class="div" v-if="show1">"I am amita"</div>
  
 </div>
</template>

<script>
export default {
  name:"home-file",
  data(){
    return {show1:true}
  },
  props: {
    //msg: String,
    demo:String,
    
  },
  methods:{
    hello(){
      // console.log("hi submit clicked");
      this.show=!this.show;
      // return{show:true}

    }
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
