<template>
  <div>
    <TodoInput v-model="newTodoText" @keydown.enter="addTodo"/>
    <TodoListItem
      v-for="todo in todos"
      :key="todo.id"
      :todo="todo"
      @remove= "removeTodo"
    />
  </div>
</template>

<script>
import TodoListItem from "./TodoListItem";
import TodoInput from "./TodoInput.vue";

let nextTodoId = 1;

export default {
  components: {
    TodoListItem,
    TodoInput
  },
  data() {
    return {
      newTodoText: "",
      todos: [
        {
          id: nextTodoId++,
          text: "item1",
        },
        {
          id: nextTodoId++,
          text: "item2",
        },
        {
          id: nextTodoId++,
          text: "item3"
        }
      ]
    }
  },
  methods: {
    addTodo() {
      const newTodoText = this.newTodoText;
      if (newTodoText) {
        this.todos.push({
          id: nextTodoId++,
          text: newTodoText,
        });
        this.newTodoText = "";
      }
    },

    removeTodo(id) {
      this.todos = this.todos.filter((todo) => {
        return todo.id !== id;
      })
    }
  }

}
</script>

<style>

</style>
