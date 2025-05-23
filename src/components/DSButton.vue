<template>
  <button 
    :class="buttonClasses"
    :disabled="disabled"
    @click="handleClick"
  >
    <slot />
  </button>
</template>

<script setup lang="ts">
import { computed } from 'vue'

export interface DSButtonProps {
  variant?: 'primary' | 'secondary'
  size?: 'small' | 'large'
  disabled?: boolean
}

const props = withDefaults(defineProps<DSButtonProps>(), {
  variant: 'primary',
  size: 'large',
  disabled: false
})

const emit = defineEmits<{
  click: [event: MouseEvent]
}>()

const buttonClasses = computed(() => {
  return [
    'btn',
    `btn-${props.variant}`,
    props.size === 'small' ? 'btn-sm' : ''
  ].filter(Boolean).join(' ')
})

const handleClick = (event: MouseEvent) => {
  if (!props.disabled) {
    emit('click', event)
  }
}
</script>

<style scoped>
/* Button styles are imported globally via main CSS */
</style> 