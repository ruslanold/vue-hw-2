<template>
    <div>
        <ul>
            <li v-for="(itemTodo, i) in arrayTodos" :key="i">
                <TodoItem 
                    :itemTodo="itemTodo" 
                />
                <button @click="deleteItem(i)">delete</button>
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
    methods: {
        deleteItem(e){
            this.$emit('deleteItem', e)
        }
    },

    
}
</script>
<style scoped>

</style>