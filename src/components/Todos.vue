<template>
    
    <div>

        <div v-bind:key="todo.id" v-for="todo in todoslist"></div>
                 
                                
                  <div>{{todo.title}}</div>
      


    </div>
</template>

<script>
export default{
    name: 'Todos',
    props: ['todoslist']
}

</script>


<style></style>