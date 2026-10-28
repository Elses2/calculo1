<script setup lang="ts">
// layout: video   ·   frontmatter: titulo, video, apunte   (NO usar `src`: Slidev la reserva)
// Con texto en el slot => video a la izquierda y texto a la derecha. Sin texto => video centrado.
defineProps<{ titulo?: string; video?: string; apunte?: string }>()
</script>

<template>
  <div class="slidev-layout video">
    <h1 v-if="titulo">{{ titulo }}</h1>
    <div class="cuerpo" :class="{ dividido: $slots.default }">
      <VideoManim v-if="video" :src="video" class="vid" />
      <div v-if="$slots.default" class="lado"><slot /></div>
    </div>
    <p v-if="apunte" class="apunte">Apunte {{ apunte }}</p>
  </div>
</template>

<style scoped>
.video { display: flex; flex-direction: column; padding: 2rem 3rem 1.6rem; }
h1 { font-size: 1.7rem; margin: 0 0 0.8rem; }
.cuerpo { flex: 1; display: flex; align-items: center; justify-content: center; gap: 2rem; min-height: 0; }
.cuerpo.dividido .vid { flex: 1.5; min-width: 0; }
.lado { flex: 1; font-size: 0.95rem; }
.apunte { align-self: flex-end; color: var(--gris-rosado); font-size: 0.75rem; margin: 0.4rem 0 0; }
</style>
