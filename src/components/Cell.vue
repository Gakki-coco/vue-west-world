<template>
  <div>
    {{ n }}
    <div class="cell" @click="onClickSelf">
      <template v-if="x">{{ text }}</template>
      <template v-else></template>
    </div>
  </div>

</template>

<script>

export default {
  name: 'Cell',
  props: ['n'],
  data() {
    return {
      x: false,
      text: null
    }
  },
  methods: {
    onClickSelf() {
      if (this.text !== null) {
        return
      }
      this.x = true
      this.text = this.n % 2 === 0 ? 'x' : 'o'
      this.$emit('click')
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
