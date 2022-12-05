<template lang="">
  <div>
    <input type="text" v-modal="todo" />
    <p>{{ todo }}</p>
  </div>
</template>
<script setup>
  import { ref } from 'vue';
  const todo = ref('');
</script>
<style lang=""></style>
