<template>
    <div>

    </div>
</template>

<script>
import axios from 'axios';

    export default {
        




        mounted(){

            axios({
                method: `GET`,
            
                url:`https://reqres.in/api/users`
            

            })


        }
    }
</script>

<style scoped>

</style>