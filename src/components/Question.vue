<template>
  <p>{{ quiz.questions[0].question }}</p>
</template>

<script setup>
const props = defineProps({
  quiz: Object,
});


</script>
