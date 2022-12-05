<template lang="">
  <div>
    <input
      type="text"
      v-model="todo"
      @change="addItem(todo)"
      placeholder="Új feladat megadása"
    />
    <!-- <ul>
      <li v-for="todo in todoList">{{ todo }}</li>
    </ul> -->
    <table>
      <tr v-for="todo in todoList">
        <td>{{ todo }}</td>
        <td><span class="btn btn-danger">Törlés</span></td>
      </tr>
    </table>
  </div>
</template>
<script setup>
  import { ref } from 'vue';
  const todo = ref(null);
  const todoList = ref(new Set());
  function addItem(t) {
    todoList.value.push(t);
    todo.value = '';
  }
</script>
<style lang=""></style>
