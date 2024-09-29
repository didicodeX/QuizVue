<script setup>
import Answers from "./components/Answers.vue";
import ProgressBar from "./components/ProgressBar.vue";
import Question from "./components/Question.vue";
import { onMounted, ref } from "vue";

const quiz = ref(null);

const color = ref()

onMounted(() => {
  fetch("/quiz.json")
  .then((response) => response.json())
  .then((data) => quiz.value = data)
});

</script>

<template>
  <div class="quiz" v-if="quiz">
    <h2 class="quiz__title">{{ quiz.title }}</h2>
    <ProgressBar :quiz/>
    <Question :quiz/>
    <Answers :quiz/>
    <button>Question suivante</button>
  </div>

  <select name="" id="" v-model="color">
    <option value="red">red</option>
    <option value="green">green</option>
    <option value="blue">blue</option>
  </select>
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
  max-width: 600px;
  row-gap: 15px;
  color: v-bind(color);
}
.quiz__title {
  text-decoration: underline;
  text-decoration-thickness: 5px;
  text-underline-offset: 6px;
  text-align: center;
}
button {
  align-self: end;
}
</style>
