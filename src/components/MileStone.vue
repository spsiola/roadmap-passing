<template>
  <div>
    Выводим майлстоун!
    <p v-for="(stone, index) in mileStones" @click="doneStone(index)" :key="index">
      {{ index }}: {{ stone }}
    </p>
  </div>
</template>
<script>
export default {
  props: ["mileStones"],
  methods: {
      doneStone(index){
          this.$emit('done-stone', index)
      }
  }
};
</script>
<style>
</style>