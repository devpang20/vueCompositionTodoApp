<template>
  <section class="todoapp">
    <Header v-model="newTodoText" @keydown.enter="addTodo" />
    <section class="main">
      <input id="toggle-all" class="toggle-all" type="checkbox"/>
      <label html-for="toggle-all">Mark all as complete</label>
      <ul class="todo-list">
        <Todo v-for="todo in todos" :key="todo.id" :todo="todo" @remove="removeTodo" />
      </ul>
    </section>
  </section>
</template>

<script>
import Todo from './Todo.vue'
import Header from "./Header.vue"

let nextTodoId = 1;

export default {
  components: {
    Todo,
    Header,
  },
  data () {
    return {
      newTodoText: "",
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
    addTodo() {
    console.log(1);
    const newTodoText = this.newTodoText;
      if (newTodoText) {
        this.todos.push({
          id: nextTodoId++,
          text: newTodoText,
        })
        this.newTodoText = "";
      }
    },
    removeTodo(id) {
      this.todos = this.todos.filter(todo => {
        return todo.id !== id;
      })
      console.log(id);
    }
  }
}
</script>

<style>

</style>
