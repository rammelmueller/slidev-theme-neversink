<script setup lang="js">
import { computed } from 'vue'

const props = defineProps({
  color: {
    default: 'white',
  },
})

const colorscheme = computed(() => {
  return `neversink-${props.color}-scheme`
})
</script>
<template>
  <div class="slidev-layout default slidecolor" :class="colorscheme">
    <slot />
    <div class="note absolute bottom-3">
      <slot name="note" />
    </div>
  </div>
</template>
