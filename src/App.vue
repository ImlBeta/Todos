
<template>

<div>
<div id="header"></div>

<div id="main-container"> 
   <h2>Todos</h2>
  
  <Todos v-bind:todoslist="copyTodos" />
    
</div>

</div>



</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
//import Search from './components/Search'
//import TodoAdd  from './components/TodoAdd'
//import TodoItem from './components/TodoItem'
import Todos  from './components/Todos'
//import Todos from './components/Todos.vue';


export default {
  name: 'App',
  components: {
    Todos
      },
  data() {
    return{
      todos: [
        {
          id: 0,
          title: 'comprar la cena',
          completed: false         
          },
         {
          id: 1,
          title: 'sacar a pasear al perro',
          completed: true         
          },
          {
          id: 2,
          title: 'Jugar Xbox',
          completed: false         
          }      
          ],
      copyTodos: []
     } 
  },
  created() {
    this.copyTodos= [... this.todos];
  }, 

}
</script>

<style>
*{
  box-sizing: border-box;
}

body {
  font-family:  Arial, Helvetica, sans-serif;
  font-size: 1.5em;
  padding: 0;
  margin: 0;

}

#main-container
{

border: solid 5px #ccc;



/* width: 600px; */

/* margin: 100px auto; */

/* border: 5px solid darkblue; */

text-align: center;

height: 50px;

margin-top: 5px;

margin-right: 5px;

margin-bottom: 8px;


}

#header{
  background: black;
  padding: 10px;
}

h2{
  text-align: center;
  padding: 0 10px;
}

</style>


