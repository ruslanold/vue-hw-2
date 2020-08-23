<template>
  <div>
    <AddTodo @updateTodoList="update"/>
    <TodoList 
      @deleteItem="deleteItem"
      :arrayTodos="arrayTodos"
    />
  </div>
</template>

<script>
import AddTodo from './components/AddTodo.vue'
import TodoList from './components/todo/TodoList.vue'

export default {
  name: 'App',
  components: {
    AddTodo,
    TodoList
  },
  data() {
    return {
      arrayTodos: []
    }
  },
  methods: {
    update(e) {
      this.arrayTodos.push(e)
    },
    deleteItem(e){
      this.arrayTodos.splice(e, 1)
    }

  } 
}
</script>

<style>
</style>
