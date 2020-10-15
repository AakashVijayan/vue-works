<template>
  <div >
<UserProfile />
    <Task />
    <br>
       Form Task
     <div>
       <Form />
       </div> 

<TextDisplay />

<br>
<ConditionRenders />

<Composition />


<CompisitionApi />
  </div>
</template>

<script>
//Task,Form,TextDisplay,ConditionRenders,Composition
import UserProfile from './components/UserProfile'; 
import Task from './components/Task';
import Form from './components/Form';
import TextDisplay from './components/TextDisplay';
import ConditionRenders from './components/ConditionRenders';
import Composition from './components/Composition';
import CompisitionApi from './components/CompisitionApi';
export default {
  name: 'App',
  components:{UserProfile,Task,Form,TextDisplay,ConditionRenders,Composition,CompisitionApi}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  min-height: 100vh;
  background-color: #F3F5FA;
}
#button{
  width: 2;
}
</style>
