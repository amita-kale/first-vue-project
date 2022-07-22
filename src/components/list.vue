<template>
    <div>
        <table border="2">
            <tr>
                <th>Sr.No</th>
                <th>Name</th>
                <th>Email</th>
            </tr>
            <tr v-for="stud in students" :key="stud.id">
                <td>{{stud.id}}</td>
                <td>{{stud.name}}</td>
                <td>{{stud.email}}</td>
            </tr>
        </table>
    </div>
</template>
<script>
export default {
  name:"list-file",
  data(){
    return {
    students:[
        {id:1,name:'amita',email:'amita@45gmail.com'},
        {id:2,name:'priyanka',email:'priyanka@12gmail.com'}
    ]
    }
  }
//   props: {
//     //msg: String,
//     demo:String,
//   }
  }
</script>