<script setup>
import Answers from './components/Answers.vue';
import ProgressBar from './components/ProgressBar.vue';
import Question from './components/Question.vue';

</script>

<template>
  <div class="quiz">
    <div class="quiz__title">Questionnaire sur les Films et series</div>
    <ProgressBar/>
    <Question/>
    <Answers/>
  </div>

</template>

<style scoped>

.quiz {
  display: flex;
  flex-direction: column;
  border: 3px solid crimson;
  justify-content: center;
  padding: 10px;
}

</style>
