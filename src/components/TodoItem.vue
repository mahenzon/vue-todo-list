<template lang="pug">
  div(v-bind:class="{'is-completed': todo.completed}").todo-item
    p
      input(type="checkbox" v-on:change="markComplete" v-bind="{checked: todo.completed}")
      span {{ todo.title }}
      button(@click="$emit('del-todo', todo.id)").del X
</template>


<script>
export default {
  name: 'TodoItem',
  props: ['todo'],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed
    }
  }
}
</script>


<style scoped>
  .todo-item {
    background: #f4f4f4;
    padding: 10px;
    border-bottom: 1px #ccc dotted;
  }

  .is-completed {
    text-decoration: line-through;
  }

  .del {
    background: #f00;
    color: #fff;
    border: none;
    padding: 5px 9px;
    border-radius: 50%;
    cursor: pointer;
    float: right;
  }
</style>
