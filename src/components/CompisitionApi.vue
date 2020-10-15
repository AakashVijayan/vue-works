<template>
    <div class="calculator">
        <h1>Simple Calculator</h1>
        <form class = "calc-form">
            <input type="text" v-model="num1"  class="field" maxLength = "2"/>
            <span class="operator">+</span>
            <input type="text" class="field" v-model="num2" maxLength = "2"/>
            <span class="operator">=</span>
            <span class="result">{{result}}</span>
        </form>
    </div>
</template>

<script>
//import { ref } from 'vue';
import { reactive, computed , toRefs} from 'vue';

function addNumbers(){
    let state = reactive({
    num1: 0,
    num2: 0,
    result : computed(()=>parseInt(state.num1) + parseInt(state.num2))
     });
     return toRefs(state);
}
export default {
    name : 'CompisitionApi',
    setup(){
        // let num1 =ref(0);
        // let num2 =ref(0);
        // let result = ref(0);
        // let state = reactive({
        //     num1:0,
        //     num2:0,
        //     result: computed(() => parseInt(state.num1) + parseInt(state.num2)),
        // });

    let{num1, num2,result} = addNumbers();

        return{
           num1,num2,result,
        }; 
    },
}


</script>


<style>
 
</style>