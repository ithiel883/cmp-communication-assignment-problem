<template class="p-4">
<label>
    Username
 <input type="text" v-model="username" class="bg-red-500">
</label>
   

<label>
    Age
 <input type="text" v-model="age" class="bg-red-500">
</label>
<button @click="addUser"> Add User</button>
</template>

<script>
export default {
    emits: [
        'add-user'
    ],
    data() {
        return  {
            username: '',
            age: ''
        }
    },
    methods: {
        addUser() {
            this.$emit('add-user', this.username, this.age)
            this.username = ''
            this.age = ''
        }
    }
}
</script>

<style>

</style>