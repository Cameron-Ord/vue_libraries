<template>
    <div>

        <span v-for="(user, i) in users" :key="i" >

            <h1> {{ user.first_name }} - {{ user.last_name }}</h1>

            <img v-bind:src="user.avatar">
            
        </span>



    </div>
</template>

<script>
import axios from 'axios';

    export default {
        


        data() {
            return {
                users:[]
            }
        },



        mounted(){

            axios({
                method: `GET`,
            
                url:`https://reqres.in/api/users`
            


            }).then((response) => {

                console.log(`success`);

                console.log(response);
                
                for(let i = 0; i < response[`data`][`data`].length; i = i +1 ){


                    this.users.push(response[`data`][`data`][i]);


                }
                
              

            }).catch((error) => {


                console.log(`fail`);

                console.log(error);
            });


        }
    }
</script>

<style scoped>

</style>