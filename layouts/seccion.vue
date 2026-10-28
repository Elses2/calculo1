<script setup lang="ts">
// Diapositiva clara para separar bloques: contrasta con las oscuras y descansa la vista.
defineProps<{ numero?: string | number }>()
</script>

<template>
  <div class="slidev-layout seccion">
    <span v-if="numero !== undefined" class="num">{{ numero }}</span>
    <div class="txt"><slot /></div>
  </div>
</template>

<style scoped>
.seccion { background: var(--rosa-claro); display: flex; align-items: center; gap: 3rem; padding: 3rem 5rem; }
.num { font-size: 12rem; font-weight: 900; line-height: 1; color: var(--magenta); }
.txt { color: var(--navy); }
.txt :deep(h1) { color: var(--navy); font-size: 2.6rem; margin: 0 0 0.4rem; }
.txt :deep(.katex) { color: var(--navy); }
.txt :deep(p) { color: var(--navy); opacity: 0.8; font-size: 1.2rem; }
</style>
