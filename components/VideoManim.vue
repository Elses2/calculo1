<script setup lang="ts">
// Reproduce el video desde el inicio cuando la slide se ve, y lo pausa cuando se oculta.
import { ref, onMounted, onBeforeUnmount } from 'vue'

const props = withDefaults(defineProps<{
  src: string
  loop?: boolean
  controls?: boolean
  ancho?: string
}>(), { loop: true, controls: false, ancho: '100%' })

const el = ref<HTMLVideoElement>()
let io: IntersectionObserver | undefined

onMounted(() => {
  io = new IntersectionObserver(([e]) => {
    const v = el.value
    if (!v) return
    if (e.isIntersecting) { v.currentTime = 0; v.play().catch(() => {}) }
    else v.pause()
  }, { threshold: 0.6 })
  if (el.value) io.observe(el.value)
})
onBeforeUnmount(() => io?.disconnect())
</script>

<template>
  <video
    ref="el"
    class="manim-video"
    :src="src"
    :loop="loop"
    :controls="controls"
    :style="{ width: ancho }"
    muted
    playsinline
    preload="auto"
  />
</template>
