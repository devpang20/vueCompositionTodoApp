<template>
  <li :class="{ completed: todo.done}">
    <div class="view">
      <input class="toggle" type="checkbox" :checked="todo.done"/>
      <label>{{ todo.text }}</label>
      <button class="destroy" />
    </div>
    <input class="edit" value="Create a TodoMVC template" />
  </li>
</template>

<script>
export default {
  props: {
    todo: {
      type: Object
    }
  },
  data () {
    return {

    }
  },
  methods: {

  }
}
</script>

<style>

</style>
