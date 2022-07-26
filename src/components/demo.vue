<template>
<div>
    <h1 v-if="show" :style="{color:mycolor}">{{Title}}</h1>
    <h1>{{count}}</h1>
    
    <br>
   Name: <input type="text" placeholder="Enter Name" v-model="msg"> 
   <h3>Msg is:{{msg}}</h3> <br>
   Pick Any Color: <input type="color" v-model="mycolor">  <br>

    <br>
    <button @click="buttonClicked()">click Here</button>
</div>
</template>
<script>
export default {
  name:"listFile",
  data(){
    return {Title:"Welcome to my page",name:"Amita",count:0,msg:'', mycolor : '#00FF00',
    show : true}
  },
 
  methods:{
    buttonClicked(){
      this.count++;
      
    }
  },
  
}
// let userData =({
//     mycolor : '#00FF00',
//     show : true
// })
</script>
