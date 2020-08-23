<template>
    <div>{{itemTodo}}</div>
</template>
<script>
export default {
    name: 'TodoItem',
    props: {
        itemTodo: {
            type: String,
            required: true
        }
    }
}
</script>
<style scoped>

</style>