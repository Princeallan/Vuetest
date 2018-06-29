<template>
    <div id="app">


        <employeestable></employeestable>
        <home></home>

    </div>
</template>

<script>
    import employees from '../src/components/employeesList.vue'
    import home from '../src/components/index.vue'

    export default {
        name: 'app',
        data() {
            return {

            }

        },
        components: {

            'employeestable': employees,
            'home':home
        }
    }



</script>
