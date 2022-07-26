<template>
<div>
    <h1>{{Title}}</h1>
    <br>
   Name: <input type="text" placeholder="Enter Name" ref="name">  <br>
    <br>
    <button>click Here</button>
</div>
</template>
<script>
export default {
  name:"listFile",
  data(){
    return {Title:"Welcome to my page",name:"Amita"}
  },
  methods:{
    buttonClicked(){
    //   this.name="Rutika"
    }
  }
}
</script>
