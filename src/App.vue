<template>
   <section>
        <active-user :username="user.name" :age="user.age"></active-user>
        <user-data @save-data="saveUserData"></user-data>    
   </section> 
</template>

<script>
export default {
    data(){
        return{
            user: {
                name:'Rajaruban',
                age: 36
            }
        }
    },
    methods:{
        saveUserData(name,age){
            this.user = {
                name: name,
                age: +age //adding + infront of value converts String into Number value
            },
            this.users.push(this.user)
        }
    }
};
</script>

<style>
html {
    font-family: sans-serif;
}

section {
    margin: 2rem auto;
    max-width: 40rem;
    border-radius: 12px;
    border: 1px solid #ccc;
    padding: 1rem;
}
</style>