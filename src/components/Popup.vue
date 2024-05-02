<template>
  <div>
    <p>This is popup message</p>
    <button @click="$emit('close', 'esther')">Close popup</button>
  </div>
</template>

<script>
export default {
  name: 'Popup',
  emits: ['close']
}
</script>

<style scoped></style>
