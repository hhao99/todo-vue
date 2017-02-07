<template>
  <div id="todoitem">
    <li>
      {{todo.text}}
      <button v-show="!todo.done" @click='removeItem'>X</button>
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
