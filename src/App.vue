<template>
  <div id="app">
    <MileStone :mile-stones="mileStones" @done-stone='doneStone' />
  </div>
</template>

<script>
import MileStone from './components/MileStone.vue'

export default {
  name: 'App',
  data(){
    return {
      mileStones: ['Internet','HTML','CSS','JavaScript','Version Cotrol Systems','Web Security Knoledge','Package Managers']
    }
  },
  components: {
    MileStone
  },
  methods: {
    doneStone(index){
      this.mileStones.splice(index, 1);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
