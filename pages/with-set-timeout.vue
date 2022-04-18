<template>
  <DisplayItems :items="items" />
</template>

<script setup>
const items = ref(null)
setTimeout(() => {
  items.value = [1, 2, 3, 4]
}, 300)
</script>