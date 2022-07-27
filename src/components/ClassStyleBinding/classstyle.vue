<template>
    <h1 class="changecolor">Data & Class and Style Binding</h1><br>
    <h2 v-bind:style="{color:'red'}">Style Binding</h2><br>
    <h3 v-bind:class="{display:'show',displayColor:'show'}">Class binding with object</h3>
    <h1 style="white-space:pre-line">{{msg}}</h1>
    <input type="text" v-model="msg"> <br>

    <br>
    <textarea type="text" v-model="msg" />

</template>>

<script>


export default({
name:"classStyle",
data(){
    return {show:true,msg:"Check Data Binding"};
}
})
</script>


<style scoped>
.changecolor{
    color: blue;
}
.display{
    background-color: aqua;
}
</style>