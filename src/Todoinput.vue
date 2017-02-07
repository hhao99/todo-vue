<template>
  <div id="todoinput">
     New todo: <input type='text' @keyup.enter='addItem' v-model='todo'></input>
  </div>
</template>

<script>
export default {
  name: 'todoinput',
  data() {
    return {todo: 'new ', counter: 0 }
  },
  props: ['additem'],
  methods: {
    addItem : function(e) {
      var task = e.target.value;
      this.additem(task);
      this.todo = 'new task: ' + this.counter++;
    }
  }
 
}
</script>

<style scoped>
   #todoinput {
     color: blue;
   }
</style>
