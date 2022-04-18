<template>
  <div v-if="props.items">
    <p>
      <template
        v-for="item in props.items"
        :key="item"
      >
        <p>Item: {{ item }}</p>
      </template>
    </p>
  </div>
</template>

<script setup>
const props = defineProps(['items'])

console.log('Items before loading', props.items)
watch(() => props.items, () => {
  console.log('Items after loading', props.items)
})
</script>