<script setup></script>

<template>
  <h2 v-if="num === 0">the num is zero</h2>
  <h3 v-else-if="num < 0">the num is negative</h3>
  <h3 v-else-if="num > 0">the num is positive</h3>
  <h2 v-else>not a number</h2>

  <template v-if="display">
    <h2>esther</h2>
    <h2>codevolution</h2>
    <h2>vue</h2>
  </template>

  <h2 v-show="showElement">using v-show</h2>
  <h2 v-if="showElement">using v-if</h2>
</template>

<script>
export default {
  name: 'App',
  setup() {
    return {
      num: 1,
      display: true,
      showElement: false
    }
  }
}
</script>

<style>
.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: green;
}

.sold-out {
  color: red;
}
</style>
