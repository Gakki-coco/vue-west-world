<template>
  <div>
    <div class="row">
      <Cell @click="onClickCell" :n="n"/>
      <Cell @click="onClickCell" :n="n"/>
      <Cell @click="onClickCell" :n="n"/>
    </div>
    <div class="row">
      <Cell @click="onClickCell" :n="n"/>
      <Cell @click="onClickCell" :n="n"/>
      <Cell @click="onClickCell" :n="n"/>
    </div>
    <div class="row">
      <Cell @click="onClickCell" :n="n"/>
      <Cell @click="onClickCell" :n="n"/>
      <Cell @click="onClickCell" :n="n"/>
    </div>
  </div>

</template>

<script>
import Cell from "@/components/Cell";

export default {
  name: 'App',
  components: {Cell},
  data() {
    return {n: 0}
  },
  methods: {
    onClickCell() {
      this.n += 1
    }
  }
}
</script>

<style>
.row {
  display: flex;
}
</style>
