<template>
    <div id="app">
        <form action="#">
            First name:<br>
            <input type="text" id="firstname" v-model="user.firstname">
            <br>
            Last name:<br>
            <input type="text" id="lastname" v-model="user.lastname">
            <br><br>
        </form>

        <p>First Name: {{ user.firstname }} .</p>
        <p>Last Name: {{ user.lastname }} .</p>

        <input type="text" id="input" v-model="user.message">
        <p v-bind:class="{greebody:users.length>4}">The best Destination to me this year wil be: {{ message }} .</p>

        <span v-if="users.length==3">
            <p> You have added Three Users</p>
        </span>


        <h2>Customers List</h2>
        <h5>Add Customer</h5>
        <input id="entry" type="text">
        <button type="button" @click="addUser()" id="button">Add Customer</button>
        <div>
            <li v-for="name in names" v-text="name"></li>
        </div>

        <table class="table table-hover">
            <thead>
            <tr>
                <th>Name</th>
                <th>Description</th>
                <th>Price</th>
            </tr>
            </thead>
            <tbody>
            <tr v-for="user in users">
                <td>{{user.firsname}}</td>
                <td>{{user.lastname}}</td>
                <td>{{user.message}}:-</td>
            </tr>
            </tbody>
        </table>

        <employeestable></employeestable>

    </div>
</template>

<script>
import employees from '../src/components/employeesList.vue'

    export default {
        name: 'app',
        data() {
            return {
                user: {
                    message: '',
                    firsname: '',
                    lastname: '',

                },
                users: []

            }

        },
        components: {

            'employeestable': employees
        },
        methods: {
            addUser() {
                this.users.push(this.user);
                this.user={};

            }
        }
    }



</script>

<style>
    table {
        font-family: "Helvetica Neue", Helvetica, Roboto, Arial, sans-serif;
        border-collapse: collapse;
        width: 80%;
    }

    td, th {
        border: 1px solid #dddddd;
        text-align: left;
        padding: 8px;
    }

    tr:nth-child(even) {
        background-color: #008080;
    }

    .greebody{
        background: green;
    }
</style>

