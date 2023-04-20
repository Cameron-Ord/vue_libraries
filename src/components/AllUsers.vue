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
            


            }).then((response) => {

                console.log(`success`);

              

            }).catch((error) => {

                console.log(`fail`);

            });


        }
    }
</script>

<style scoped>

</style>