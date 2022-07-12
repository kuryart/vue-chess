<script setup>
import House from './House.vue'
</script>

<template>
  <div class="board">
    <div v-for="n in 64" :key="n" class="house">
      <House />
    </div>
  </div>
</template>

<style>
.board {
  display: grid;
  grid-template-columns: repeat(8, 1fr);
  grid-template-rows: repeat(8, 1fr);
  margin: 0 auto;
  width: 512px;
}

.board>* {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #9ab;
  height: 64px;
  width: 64px;
}

.board>*:nth-child(16n+2),
.board>*:nth-child(16n+4),
.board>*:nth-child(16n+6),
.board>*:nth-child(16n+8),
.board>*:nth-child(16n+9),
.board>*:nth-child(16n+11),
.board>*:nth-child(16n+13),
.board>*:nth-child(16n+15) {
  background-color: #789;
}
</style>
