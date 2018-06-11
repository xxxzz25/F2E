<template>
  <div>
    <todoItem></todoItem>
  </div>
</template>

<script>
  import todoItem from "./todoItem";
  
  export default {
    name: "App",
    components: {
      todoItem
    },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

</style>
