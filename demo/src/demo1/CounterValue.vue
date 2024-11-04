<template>
  <span> Current value: {{props.value}} </span>
</template>

<script setup>
  const props = defineProps({
    value: {
      type: Number,
      required: true
    }
  })
</script>
