<template>
    <div>
        {{itemTodo}}
        <button @click="deleteItem">delete</button>
    </div>
</template>
<script>

import {eventBus} from '@/main'

export default {
    name: 'TodoItem',
    props: {
        itemTodo: {
            type: String,
            required: true
        },
        itemID: {
            type: Number,
            required: true
        }
    },

    methods: {
        deleteItem(){
            eventBus.$emit('deleteItem', this.itemID)
        }
    }
}
</script>
<style scoped>

</style>