<template>
  <div class="quiz__progress">
    <progress value="50" max="100"></progress>
    <span>50%</span>
  </div>
</template>

<style scoped>
.quiz__progress {
  display: flex;
  column-gap: 30px;
  align-items: center;
}
progress {
  align-self: flex-end;
}


</style>