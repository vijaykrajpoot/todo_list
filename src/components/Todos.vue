<template>
    <div >
        <div v-bind:key ="todo.id" v-for="todo in todos " >
            <TodosItems v-bind:todo="todo" 
            v-on:del-todo="$emit('del-todo',todo.id)"   />
       </div> 

    </div>
</template>

<script>

import TodosItems from './TodoItems.vue';

export default {
    name :"Todos",
    components : {
        TodosItems 
    },
    props :["todos"]
}
</script>

<style scoped>

</style>