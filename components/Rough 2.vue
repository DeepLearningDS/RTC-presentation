<script setup>
import { ref, watch, onMounted } from 'vue'
import { annotate } from 'rough-notation'

const props = defineProps({
  type: { type: String, default: 'underline' },
  color: { type: String, default: '#fbbf24' },
  strokeWidth: { type: Number, default: 2 },
  padding: { type: [Number, Array], default: 5 },
  brackets: { type: [String, Array], default: 'right' }, // Aggiunto per le parentesi
  show: { type: Boolean, default: true } // Aggiunto per controllare QUANDO disegnare
})

const elementRef = ref(null)
let annotation = null

onMounted(() => {
  if (elementRef.value) {
    annotation = annotate(elementRef.value, {
      type: props.type,
      color: props.color,
      strokeWidth: props.strokeWidth,
      padding: props.padding,
      brackets: props.brackets
    })
    
    // Disegna subito solo se show è true, altrimenti aspetta
    if (props.show) annotation.show()
  }
})

// Ascolta i cambiamenti della variabile 'show' per far partire l'animazione al click
watch(() => props.show, (newVal) => {
  if (newVal && annotation) annotation.show()
  if (!newVal && annotation) annotation.hide()
})
</script>

<template>
  <span ref="elementRef" class="inline-block">
    <slot />
  </span>
</template>