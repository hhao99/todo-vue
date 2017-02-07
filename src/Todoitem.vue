<template>
  <div id="todoitem">
    <li>
      
      <input type='checkbox' v-show="!todo.done" @click="todo.done = !todo.done"></input>
      {{todo.text}}
      <button @click='removeItem'>X</button>
    </li>
  </div>
</template>

<script>
export default {
  name: 'todoitem',
  props: ['todo','remove'],
  methods: {
    removeItem: function() {
      this.remove(this.todo);
    }
  }
}
</script>

<style scoped>
  #todoitem {
    background-color: darkgoldenrod;
  }
</style>
