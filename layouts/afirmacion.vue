<script setup lang="ts">
// Ejercicio 3 (verdadero/falso).  frontmatter: id, veredicto ('V'|'F'), apunte, video
// Slots:  ::enunciado::  (la afirmación)   y   ::default::  (justificación + contraejemplo)
defineProps<{ id?: string; veredicto?: 'V' | 'F'; apunte?: string; video?: string }>()
</script>

<template>
  <div class="slidev-layout afirmacion">
    <header>
      <span class="id">{{ id }}</span>
      <span class="sello" :class="veredicto === 'V' ? 'ok' : 'no'">
        {{ veredicto === 'V' ? 'Verdadero' : 'Falso' }}
      </span>
      <span v-if="apunte" class="apunte">Apunte {{ apunte }}</span>
    </header>

    <div class="enunciado"><slot name="enunciado" /></div>

    <div class="cuerpo">
      <div class="texto"><slot name="default" /></div>
      <VideoManim v-if="video" :src="video" class="vid" />
    </div>
  </div>
</template>

<style scoped>
.afirmacion { display: flex; flex-direction: column; gap: 0.9rem; padding: 1.8rem 3rem; }
header { display: flex; align-items: center; gap: 1rem; }
.id { font-size: 1.6rem; font-weight: 800; color: var(--rosa); }
.sello { padding: 0.15rem 0.9rem; border-radius: 999px; font-weight: 800; font-size: 0.95rem; }
.sello.ok { background: var(--menta); color: var(--navy); }
.sello.no { background: var(--magenta); color: var(--rosa-claro); }
.apunte { margin-left: auto; color: var(--gris-rosado); font-size: 0.75rem; }
.enunciado { background: var(--navy-2); border-radius: 12px; padding: 0.7rem 1.2rem; font-size: 1.05rem; }
.cuerpo { flex: 1; display: flex; gap: 2rem; align-items: center; min-height: 0; }
.texto { flex: 1; font-size: 0.95rem; }
.vid { flex: 1.3; min-width: 0; }
</style>
