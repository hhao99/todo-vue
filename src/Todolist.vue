<template>
  <div id="app">
    <section v-show='todos.length'>
      You have {{todos.length}} task(s) to be done!
      <ul v-for="todo in todos">
        <todoitem :todo='todo' v-bind:remove='removeitem'></todoitem>
      </ul>
    </section>
   </div>
</template>

<script>
import Todoitem from './Todoitem.vue'
export default {
  name: 'todolist',
  props: ['todos','remove'],
  components: {
    todoitem: Todoitem
  },
  methods: {
    removeitem: function(todo) {
      console.log("remove the item: " + todo.text);
      this.remove(todo);
    }
  }
}
</script>

<style scoped>
 
</style>
