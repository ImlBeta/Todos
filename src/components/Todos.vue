<template>

    <div>
        <div v-bind:key="todo.id" v-for="todo in todoslist">
            <TodoItem v-bind:todo="todo"/>
            
        </div>
    </div>

</template>

<script>
import TodoItem from './TodoItem.vue'
export default {
  components: { TodoItem },
    name: 'Todos',
    props: ['todoslist']
}
</script>

<style></style>
