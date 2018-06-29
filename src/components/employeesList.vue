<template>
<div id="app">


    </div>

</template>
<script>
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