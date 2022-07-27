<template>
 
<div>
  <h1 style="color:blue">signUp Form</h1>
 
 ID:<input type="number"><br><br>
 Name:<input type="text"><br><br>
 Hobbies: &nbsp;&nbsp;<input type="checkbox" id="hob">
 <label for="hob">Kho-Kho</label> &nbsp;
 <input type="checkbox" id="hobi">
 <label for="hobi">Cricket</label><br>
<br>
 Gender: &nbsp;&nbsp;<input type="radio" id="Female" name="gender">
 <label for="Female">Female</label>&nbsp;
 <input type="radio" id="male" name="gender">
 <label for="male">Male</label>
 </div>
</template>

<script>
export default {
  name:"signUpForm"
}
</script>
