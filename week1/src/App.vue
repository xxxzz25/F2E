<template>
  <div id="app">
    <navi/>
    <div class="container">
      <addTask/>
      <todoList/>
    </div>
  </div>
</template>

<script>
  import navi from "./components/nav";
  import addTask from "./components/addTask";
  import todoList from "./components/todoList";

  export default {
    name: "App",
    components: {
      navi,
      addTask,
      todoList
    }
  };
</script>

<style lang="scss">
  #app {
    background-color: #e1e1e1;
    min-height: 100vh;
    .container{
      width: 1024px;
      margin: 0 auto;
    }
  }
</style>
