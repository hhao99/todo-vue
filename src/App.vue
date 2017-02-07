<template>
  <div id="app">
    <img src="./assets/ava.png">
    <h1>{{ msg }}</h1>
    <Todobox></Todobox>
   
  </div>
</template>

<script>
import Todobox from './Todobox.vue'
export default {
  name: 'app',
  data () {
    return {
      msg: 'Todo MVC App'
    }
  },
  components: {
    Todobox
  }
}
</script>

<style scoped>
  #app {
    background: dimgrey;
    color: white;
  }
</style>
