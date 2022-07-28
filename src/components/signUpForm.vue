<template>
  <div>
    <div>
      <h1 style="color: red" class="font-bold text-3xl p-6">signUp Form</h1>

      ID:<input
        type="number"
        class="bg-white border border-slate-300 rounded-md mx-4 py-2 pl-9 pr-3"
        v-model="signUp.id"
      /><br /><br />

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
        type="submit"
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
        <tr v-for="user in users" :key="user">
          <td>{{ user.id }}</td>
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
        " v-on:click="editCliked()">Edit</button></td>
           <td><button  class="
          border-solid
          rounded
          border-2 border-indigo-600
          p-1
          bg-gradient-to-r
          from-indigo-500
          via-purple-500
          to-pink-500
        " @click="deleteClicked()">Delete</button></td>
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
      
      console.warn(this.signUp);
     this.users.push(this.signUp);
      console.log(this.users);
    this.signUp= {
        id: '',
        name: '',
        hobbies: [],
        gender: '',
      };
    },
    editCliked(){
      console.log("Edit");

    },
    deleteClicked(){
      console.log("delete");
    }
  },
      
   

 
};
</script>
