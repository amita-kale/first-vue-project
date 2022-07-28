<template>
  <div>
    <div>
      <h1 style="color: red" class="font-bold text-3xl p-6">signUp Form</h1>

      <!-- ID:<input
        type="number"
        class="bg-white border border-slate-300 rounded-md mx-4 py-2 pl-9 pr-3"
        v-model="signUp.id"
      /><br /><br /> -->

      Name:<input
        type="text"
        class="bg-white border border-slate-300 rounded-md py-2 pl-9 pr-3"
        v-model="signUp.name"
      /><br /><br />
      Hobbies: &nbsp;&nbsp;<input
        type="checkbox"
        id="hob"
        value="kho-kho"
        v-model="signUp.hobbies"
      />
      <label for="hob">Kho-Kho</label> &nbsp;
      <input
        type="checkbox"
        id="hobi"
        value="Cricket"
        v-model="signUp.hobbies"
      />
      <label for="hobi">Cricket</label><br />
      <br />
      Gender: &nbsp;&nbsp;<input
        type="radio"
        id="female"
        value="female"
        name="gender"
        v-model="signUp.gender"
      />
      <label for="female">Female</label>&nbsp;
      <input
        type="radio"
        id="male"
        value="male"
        name="gender"
        v-model="signUp.gender"
      />
      <label for="male">Male</label><br />
      <br />
      <button
        type="submit" id="submit-button"
        class="
          border-solid
          rounded
          border-2 border-indigo-600
          p-3
          bg-gradient-to-r
          from-indigo-500
          via-purple-500
          to-pink-500
        "
        v-on:click="submitFormValues()"
      >
        Submit
      </button>
    </div>
    <div>
      <table class="border border-solid">
        <tr>
          <th>ID</th>
          <th>Name</th>
          <th>Hobbies</th>
          <th>Gender</th>
          <th colspan="2">Action</th>
        </tr>
        <tr v-for="(user,index) in users" :key="user">
          <td>{{index+1}}</td>
          <td>{{ user.name }}</td>
          <td>{{ user.hobbies }}</td>
          <td>{{ user.gender }}</td>
          <td><button  class="
          border-solid
          rounded
          border-2 border-indigo-600
          p-1
          bg-gradient-to-r
          from-indigo-500
          via-purple-500
          to-pink-500
        " v-on:click="editCliked(index)">Edit</button></td>
           <td><button  class="
          border-solid
          rounded
          border-2 border-indigo-600
          p-1
          bg-gradient-to-r
          from-indigo-500
          via-purple-500
          to-pink-500
        " @click="deleteClicked(index)">Delete</button></td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>

export default {
  name: "signUpForm",
  
  data() {
    return {
      isEdit:false,
      editIndex:-1,
      users :[],
      signUp: {
        id: null,
        name: null,
        hobbies: [],
        gender: null,
      },
       };
  },
      methods: {
      submitFormValues() {
      if(this.isEdit===true){
        this.users[this.editIndex]=this.signUp;
        this.isEdit=false,
        this.editIndex=-1
        let b=document.getElementById('submit-button');
                    b.innerText='Submit';
        }
      else{
        this.users.push(this.signUp);
      }
      console.warn(this.signUp);
     
      console.log(this.users);
      this.signUp= {
          id: '',
          name: '',
          hobbies: [],
          gender: '',
        };
    },
    editCliked(i){
      console.log("Edit");
      this.signUp.id=this.users[i].id;
      this.signUp.name=this.users[i].name;
       this.signUp.hobbies=this.users[i].hobbies;
        this.signUp.gender=this.users[i].gender;
        this.isEdit=true;
      this.editIndex=i;
        let b=document.getElementById('submit-button');
                    b.innerText='Update';
    },
    deleteClicked(index){
      console.log("delete");
      this.users.splice(index,1);
    }
  },
      
   

 
};
</script>
