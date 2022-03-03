<template>
    <section>
        <form @submit.prevent="saveData">
            <div>
                <input type="text" v-model="enteredUserName" placeholder="Enter UserName.."> 
            </div>
            <div>
                <input type="number" v-model="enteredAge" placeholder="Enter age.."> 
            </div>
            <button>Set User Data</button>
        </form>
    </section>
</template>

<script>
export default {
    emits:[
        'save-data'
    ],
    data(){
        return{
            enteredUserName: '',
            enteredAge: ''
        }
    },
    methods: {
        saveData(){
            this.$emit('save-data', this.enteredUserName, this.enteredAge);
        }
    }
}
</script>

<style>

</style>