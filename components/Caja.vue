<script setup lang="ts">
// <Caja tipo="definicion|teorema|contraejemplo|nota" apunte="7.3">contenido</Caja>
import { computed } from 'vue'

const props = withDefaults(defineProps<{
  tipo?: 'definicion' | 'teorema' | 'contraejemplo' | 'nota'
  titulo?: string
  apunte?: string
}>(), { tipo: 'definicion' })

const nombres = {
  definicion: 'Definición',
  teorema: 'Teorema',
  contraejemplo: 'Contraejemplo',
  nota: 'Nota',
}
const rotulo = computed(() => props.titulo ?? nombres[props.tipo])
</script>

<template>
  <div class="caja" :class="tipo">
    <div class="cabecera">
      <span class="rotulo">{{ rotulo }}</span>
      <span v-if="apunte" class="apunte">Apunte {{ apunte }}</span>
    </div>
    <div class="cuerpo"><slot /></div>
  </div>
</template>

<style scoped>
.caja {
  --acento: var(--rosa);
  background: var(--navy-2);
  border-left: 6px solid var(--acento);
  border-radius: 0 12px 12px 0;
  padding: 0.7em 1.1em 0.8em;
  margin: 0.8em 0;
}
.caja.teorema       { --acento: var(--magenta); }
.caja.contraejemplo { --acento: var(--ambar); }
.caja.nota          { --acento: var(--gris-rosado); }

.cabecera { display: flex; justify-content: space-between; align-items: baseline; margin-bottom: 0.3em; }
.rotulo { color: var(--acento); font-weight: 800; font-size: 0.95em; }
.caja.teorema .rotulo { color: var(--rosa); }
.apunte { color: var(--gris-rosado); font-size: 0.75em; }
.cuerpo :deep(p) { margin: 0.25em 0; }
</style>
