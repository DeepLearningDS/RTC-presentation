<script setup>
import { ref, watch, onMounted } from 'vue'
import { annotate } from 'rough-notation'

const props = defineProps({
  type: { type: String, default: 'underline' },
  color: { type: String, default: '#fbbf24' },
  strokeWidth: { type: Number, default: 2 },
  padding: { type: [Number, Array], default: 5 },
  brackets: { type: [String, Array], default: 'right' },
  show: { type: Boolean, default: true },
  animationDuration: { type: Number, default: 800 },
  delay: { type: Number, default: 0 }
})

const elementRef = ref(null)
let annotation = null
let timeoutId = null // Variabile per tenere traccia del timer

onMounted(() => {
  if (elementRef.value) {
    annotation = annotate(elementRef.value, {
      type: props.type,
      color: props.color,
      strokeWidth: props.strokeWidth,
      padding: props.padding,
      brackets: props.brackets,
      animationDuration: props.animationDuration
    })
    
    if (props.show) {
      if (props.delay > 0) {
        timeoutId = setTimeout(() => annotation.show(), props.delay)
      } else {
        annotation.show()
      }
    }
  }
})

watch(() => props.show, (newVal) => {
  if (newVal && annotation) {
    if (props.delay > 0) {
      timeoutId = setTimeout(() => annotation.show(), props.delay)
    } else {
      annotation.show()
    }
  }
  if (!newVal && annotation) {
    clearTimeout(timeoutId) // Annulla il timer se cambi slide
    annotation.hide()       // Cancella il tratto rosso per il prossimo rientro
  }
})
</script>

<template>
  <span ref="elementRef" class="inline-block">
    <slot />
  </span>
</template>