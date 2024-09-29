<template>
  <ul>
    <li v-for="choice in quiz.questions[0].choices" :key="choice">
      <label><input type="radio" name="answer" />{{ choice }}</label>
    </li>
  </ul>
</template>
<script setup>
defineProps({
  quiz: Object,
});
</script>
<style scoped>
ul,
li {
  list-style: none;
}
</style>
