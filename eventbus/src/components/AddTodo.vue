<template>
  <div>
    <input v-model="value"/>
    <button @click="updateTodoList">add</button>
  </div>
</template>

<script>
export default {
  name: 'AddTodo',
  data(){
    return {
      value: ''
    }
  },
  methods: {
    updateTodoList(){
      this.$emit("updateTodoList", this.value)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
