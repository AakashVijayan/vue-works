<template>
<div>
    <button>Counter</button>    
</div>    
</template>

<script>
import { onMounted } from 'vue';
export default {
    name:"Composition",
    props:{
        chek:{type:String, default:'***'}
    },
    setup(props){
        console.log(props);

        onMounted(()=>{
            console.log("inside the onMounted")
        })
    }
}
</script>

<style>

</style>