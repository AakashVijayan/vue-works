<template>
    <Button> BUtton is clicked {{count}} times</Button>
</template>

<script>

export default {
    name:"BUttonClickDisplay",
    data(){
        return{
            name:"TweetItem"
props:{
    clicked:{
     required: true
    },
        }
    }
}
}
</script>

<style>

</style>