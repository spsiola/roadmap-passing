<template>
  <div>
    Выводим майлстоун!
    <p v-for="(stone, index) in mileStones" :key="index">
      {{ index }}: {{ stone }}
    </p>
  </div>
</template>
<script>
export default {
  props: ["mileStones"],
};
</script>
<style>
</style>