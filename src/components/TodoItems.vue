<template>
  <div class="todo-items"  v-bind:class = "{'isCompleted': todo.completed}" >
    <p> 
      <input type="checkbox" v-on:change ="markComplete"  />
      {{todo.title}} 
      <button  @click="$emit('del-todo',todo.id)" class="del" >x</button>   
      </p>
  </div>
</template>

<script>
export default {
    name: "TodoItems",
    props :["todo"],
    methods :{
       markComplete(){
           this.todo.completed=!this.todo.completed;
       }     
    }
}
</script>

<style scoped>
.todo-items {
    background: whitesmoke;
    padding: 10px;
    color: black;
    border-bottom : 1 px #000000 dotted ;
}

.isCompleted {
    text-decoration: line-through;
}
.del {
    background: red;
    color: white;
    padding: 5px 9px;
    border-radius: 50%;
    cursor: pointer;
    float: right; 
}


</style>