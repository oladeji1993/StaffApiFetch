<template>
    <div>
        <h1>Question 1. (STAFFS LIST)</h1>
    <div>
        <table>
            <tr>
                <th>Name</th>
                <th>Salary</th>
                <th>Age</th>
            </tr>
            <tr :key="item.id" v-for="item in list">
                <td>{{item.employee_name}}</td>
                <td>{{item.employee_salary}}</td>
                <td>{{item.employee_age}}</td>
            </tr>
        </table>
        </div>
    </div>
</template>

<script>

import { createApp } from 'vue';
import axios from 'axios';
import VueAxios  from 'vue-axios'


const app = createApp()
app.use(VueAxios, axios )

export default {

    name: "StaffList",
    data(){
        return {list : undefined }
    },

    mounted(){
        app.axios.get('http://dummy.restapiexample.com/api/v1/employees')
        .then((resp) =>{
            this.list = resp?.data?.data
            console.log(resp?.data?.data)
        })
    }

}

</script>



<style>
table {
  font-family: arial, sans-serif;
  border-collapse: collapse;
  width: 100%;
}

td, th {
  border: 1px solid #dddddd;
  text-align: left;
  padding: 8px;
}

tr:nth-child(even) {
  background-color: #dddddd;
}
</style>
