<template>
  <div 
    :class="inputClasses"
    @click="handleClick"
    @mouseenter="handleMouseEnter"
    @mouseleave="handleMouseLeave"
  >
    <!-- XS and Small sizes -->
    <template v-if="size === 'xs' || size === 'small'">
      <span>{{ label }}</span>
    </template>
    
    <!-- Medium size with side label -->
    <template v-else-if="size === 'medium'">
      <span class="box-input-main-label">{{ label }}</span>
      <span v-if="sideLabel" class="box-input-side-label">{{ sideLabel }}</span>
    </template>
    
    <!-- Large size with description -->
    <template v-else-if="size === 'large'">
      <div class="box-input-label">{{ label }}</div>
      <div v-if="description" class="box-input-description">{{ description }}</div>
    </template>
  </div>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue'

export interface DSBoxInputProps {
  size?: 'xs' | 'small' | 'medium' | 'large'
  label: string
  sideLabel?: string
  description?: string
  state?: 'default' | 'hover' | 'selected' | 'focus'
}

const props = withDefaults(defineProps<DSBoxInputProps>(), {
  size: 'small',
  state: 'default'
})

const emit = defineEmits<{
  click: [event: MouseEvent]
  stateChange: [state: string]
}>()

const currentState = ref(props.state)

const inputClasses = computed(() => {
  const sizeClass = props.size === 'xs' ? 'box-input-xs' :
                   props.size === 'small' ? 'box-input-sm' :
                   props.size === 'medium' ? 'box-input-md' :
                   'box-input-lg'
  
  const stateClass = `box-input-${currentState.value}`
  
  return [
    'box-input',
    sizeClass,
    stateClass
  ].join(' ')
})

const handleClick = (event: MouseEvent) => {
  currentState.value = currentState.value === 'selected' ? 'default' : 'selected'
  emit('click', event)
  emit('stateChange', currentState.value)
}

const handleMouseEnter = () => {
  if (currentState.value === 'default') {
    currentState.value = 'hover'
    emit('stateChange', currentState.value)
  }
}

const handleMouseLeave = () => {
  if (currentState.value === 'hover') {
    currentState.value = 'default'
    emit('stateChange', currentState.value)
  }
}
</script>

<style scoped>
/* Box input styles are imported globally via main CSS */
</style> 