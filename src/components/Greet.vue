<template>
  <h2>hello {{ name }} a.k.a {{ nickName }}</h2>
</template>

<script>
export default {
  name: 'Greet',
  props: ['name', 'nickName']
}
</script>

<style scoped></style>
