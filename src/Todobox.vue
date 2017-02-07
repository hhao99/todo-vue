<template>
  <div id="todobox">
    <todoinput v-bind:additem='additem'></todoinput>
    <todolist v-bind:todos='todos' v-bind:remove="removeitem"></todolist>
    <todoinput v-bind:additem='additem' v-show="todos.length"></todoinput>
  </div>
</template>

<script>
import Todolist from './Todolist.vue'
import Todoinput from './Todoinput.vue'
export default {
  name: 'todobox',
  data: function () {
    return {
      todos: [
        {'text': '1st task', done: false},
        {'text': '2nd task', done: true}
      ]
    }
  },
  methods: {
    additem: function(item){
      var task = { text: item, done:false};
      this.todos.push(task);
    },
    removeitem: function(todo) {
      this.todos.splice(this.todos.indexOf(todo),1);
    }
  },
  components: {
    Todolist, Todoinput
  }
}
</script>

<style scoped>
 
</style>
