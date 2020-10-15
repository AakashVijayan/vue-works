<template>
<div>
    <p>Condtiton Renders Task</p>
    <h1 v-show="false">Hello!</h1>
    <p v-if="employee.id == 0" >{{employee.name}}</p>
    <p v-else-if="employee.age >= 15" >{{employee.age}}</p>
    <p v-else>NO user Found</p>
</div>    
</template>

<script>
export default {
    name:"ConditionRenders",
    data(){
        return{
            employee:{
                id:1,
                name:"Aakash",
                age:20
            }
        }
    }
}
</script>

<style>

</style>