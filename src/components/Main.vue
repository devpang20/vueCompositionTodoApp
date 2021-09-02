<template>
  <section class="main">
    <input id="toggle-all" class="toggle-all" type="checkbox"/>
    <label html-for="toggle-all">Mark all as complete</label>
      <ul class="todo-list">
        <li class="completed">
          <div class="view">
            <input class="toggle" type="checkbox"  checked />
            <label>Taste JavaScript</label>
            <button class="destroy" />
          </div>
          <input class="edit" value="Create a TodoMVC template" />
        </li>
    </ul>
  </section>
</template>

<script>
export default {

}
</script>

<style>

</style>
