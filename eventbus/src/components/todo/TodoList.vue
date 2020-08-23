<template>
    <div>
        <ul>
            <li v-for="(itemTodo, itemID) in arrayTodos" :key="itemID">
                <TodoItem 
                    :itemTodo="itemTodo"
                    :itemID="itemID"
                />
            </li>
        </ul>
    </div>
</template>
<script>
import TodoItem from "./TodoItem.vue";
export default {
    name: 'TodoList',
    components: {TodoItem},
    props: {
        arrayTodos: {
            type: Array,
            required: true,
        }
    },


    
}
</script>
<style scoped>

</style>