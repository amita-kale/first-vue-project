<template>
    <h1 class="changecolor">Class and Style Binding</h1><br>
    <h2 v-bind:style="{color:'red'}">Style Binding</h2><br>
    <h3 v-bind:class="{display:show,displayColor:show}">Class binding with object</h3>

</template>>

<script>


export default({
name:"classStyle",
data(){
    return {show:true};
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