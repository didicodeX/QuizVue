<script setup>
import Answers from './components/Answers.vue';
import ProgressBar from './components/ProgressBar.vue';
import Question from './components/Question.vue';

</script>

<template>
  <div class="quiz">
    <h1 class="quiz__title">Quiz sur les Films et series</h1>
    <ProgressBar/>
    <Question/>
    <Answers/>
  </div>

</template>

<style scoped>

.quiz {
  display: flex;
  flex-direction: column;
  box-shadow: 0px 0px 2px 2px rgba(255, 255, 255, 0.3);
  justify-content: center;
  border-radius: 7px;
  padding: 20px;
  margin: 20px auto;
  max-width: 500px;
  row-gap: 15px;
}
.quiz__title {
  text-decoration: underline;
  text-decoration-thickness: 5px;
  text-underline-offset: 6px;
  text-align: center;
}

</style>
