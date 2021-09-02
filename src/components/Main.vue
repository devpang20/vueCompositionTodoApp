<template>
  <section class="main">
    <input id="toggle-all" class="toggle-all" type="checkbox"/>
    <label html-for="toggle-all">Mark all as complete</label>
    <ul class="todo-list">
      <Todo v-for="todo in todos" :key="todo.id" :todo="todo" />
    </ul>
  </section>
</template>

<script>
import Todo from './Todo.vue'

let nextTodoId = 1;

export default {
  components: { Todo },
  data () {
    return {
      todos: [
        {
          id: nextTodoId++,
          text: "item1",
          done: true
        },
        {
          id: nextTodoId++,
          text: "item2",
          done: false
        },
        {
          id: nextTodoId++,
          text: "item3",
          done: true
        }
      ]
    }
  },
  methods: {
  }
}
</script>

<style>

</style>
