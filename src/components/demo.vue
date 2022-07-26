<template>
<div>
    <h1>{{name}}</h1>
    <br>
    <button>click Here</button>
</div>
</template>
<script>
export default {
  name:"listFile",
  data(){
    return {name:"Welcome to my page"}
  },
  methods:{
    buttonClicked(){
    //   this.name="Rutika"
    }
  }
}
</script>
