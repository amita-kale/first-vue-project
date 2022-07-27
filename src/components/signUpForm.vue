<template>
 
<div>
  <h1 style="color:blue">signUp Form</h1>
 
 ID:<input type="number" v-model="signUp.id"><br><br>
 Name:<input type="text" v-model="signUp.name"><br><br>
 Hobbies: &nbsp;&nbsp;<input type="checkbox" id="hob" v-model="signUp.hobbies">
 <label for="hob">Kho-Kho</label> &nbsp;
 <input type="checkbox" id="hobi" v-model="signUp.hobbies">
 <label for="hobi">Cricket</label><br>
<br>
 Gender: &nbsp;&nbsp;<input type="radio" id="female" value="female" name="gender" v-model="signUp.gender">
 <label for="female">Female</label>&nbsp;
 <input type="radio" id="male" value="male" name="gender" v-model="signUp.gender">
 <label for="male">Male</label><br>
 <br>
 <button type="submit" v-on:click="submitFormValues()">Submit</button>
 </div>
</template>

<script>
export default {
  name:"signUpForm",
  data(){
    return {
      signUp:{
      id:null,
      name:null,
      hobbies:[],
      gender:null
    }}
  },
  methods:{
    submitFormValues(){
      console.warn(this.signUp);
    }
  }
}
</script>
