<template>
  <DisplayItems :items="items" />
</template>

<script setup>
const { pending, data: items } = useAsyncData('tasks', () => $fetch('/api/items'))
</script>