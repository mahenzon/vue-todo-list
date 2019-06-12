<template lang="pug">
  header.header
    h1 TodoList
    div#nav
      router-link(to="/") Home |
      router-link(to="/about") About
</template>


<script>
export default {
  name: 'Header',
}
</script>

<style scoped>
  .header {
    background: #333;
    color: #fff;
    text-align: center;
    padding: 10px;
  }

  .header a {
    color: #fff;
    padding-right: 5px;
    text-decoration: none;
  }
</style>
