<template>
 
 <div>
  <!-- <h1>Hello</h1> -->
  <h2>{{demo}}</h2>
  <button v-on:click="hello()">Submit</button>
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
      console.log("hi submit clicked");
    }
  }
}
</script>
