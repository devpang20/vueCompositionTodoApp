<template>
  <header class="header">
    <h1>todos</h1>
    <input class="new-todo" placeholder="What needs to be done" :value="value" v-on="listeners" autofocus />
  </header>
</template>

<script>
export default {
  props: {
    value: {
      type: String,
      default: ""
    }
  },
  computed: {
    listeners() {
      return {
        ...this.$listeners,
        input: (e) => this.$emit("input", e.target.value),
      };
    },
  },
}
</script>

<style>

</style>
