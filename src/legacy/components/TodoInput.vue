<template>
  <div>
    <input type="text" :value="value" v-on="listeners" />
  </div>
</template>

<script>
export default {
  props: {
    value: { type: String, default: ""},
  },
  computed: {
    listeners() {
      return {
        ...this.$listeners,
        input: (e) => this.$emit("input", e.target.value),
      }
    }
  }
}
</script>

<style>

</style>
