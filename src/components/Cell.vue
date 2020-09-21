<template>
  <div class="cell" @click="x = true">
    <template v-if="x">{{ text }}</template>
    <template v-else></template>
  </div>
</template>

<script>

export default {
  name: 'Cell',
  data() {
    return {
      x: false,
      text: 'x'
    }
  }
}
</script>

<style>
.cell {
  border: 1px solid black;
  width: 100px;
  height: 100px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 80px;
}
</style>
