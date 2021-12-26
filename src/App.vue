<template>
<h1 class="text-3xl font-bold underline"> 
User Registerer
</h1>
<active-user
v-for="user in users"
:key="user.id"
:id="user.id"
:username="user.username"
:age="user.age"
>

</active-user>
<user-data
@add-user="addUser"
></user-data>

</template>

<script>
export default {
    data() {
        return {
            users: [
                {
                    id: 'user1',
                    username: 'user2',
                    age: '44'
                }, 
                {
                    id: 'user2',
                    username: 'user2',
                    age: '29'
                }
            ]
        }
    },
    methods: {
        addUser(username, age) {
            const newUser = {
                id: new Date().toISOString(),
                username: username,
                age: age
            }
            this.users.push(newUser)
            username = ''
            age = ''
        }
    }
}
</script>


<style>

</style>