<script setup lang="ts">
defineProps<{ titulo?: string; subtitulo?: string; materia?: string; grupo?: string }>()

// Curva decorativa: f(x) = x²·e^(−x²) completa (Ejercicio 1.a), con sus 3 puntos críticos.
const W = 420, base = 200, k = 420, xmax = 3.2
const f = (x: number) => x * x * Math.exp(-x * x)
const X = (x: number) => ((x + xmax) / (2 * xmax)) * W
const Y = (y: number) => base - y * k
let d = ''
for (let x = -xmax; x <= xmax + 1e-6; x += 0.05) d += (d ? 'L' : 'M') + X(x).toFixed(1) + ' ' + Y(f(x)).toFixed(1)
const criticos = [-1, 0, 1].map(x => ({ cx: X(x), cy: Y(f(x)) }))
</script>

<template>
  <div class="slidev-layout portada">
    <div class="contenido">
      <div class="materia">{{ materia }}</div>
      <h1>{{ titulo }}</h1>
      <div class="subtitulo">{{ subtitulo }}</div>
      <span class="grupo">{{ grupo }}</span>
      <slot />
    </div>
    <svg class="deco" :viewBox="`0 0 ${W} 240`" aria-hidden="true">
      <line x1="0" :y1="base" :x2="W" :y2="base" stroke="#2B2D4D" stroke-width="2" />
      <path :d="d" fill="none" stroke="#FB90B7" stroke-width="6" stroke-linecap="round" stroke-linejoin="round" />
      <circle v-for="(p, i) in criticos" :key="i" :cx="p.cx" :cy="p.cy" r="8.5"
              fill="#47D19F" stroke="#0F1021" stroke-width="3" />
    </svg>
  </div>
</template>

<style scoped>
.portada { position: relative; display: flex; align-items: center; padding: 0 4rem; overflow: hidden; }
.contenido { position: relative; z-index: 1; max-width: 50%; }
.materia { color: var(--gris-rosado); font-size: 0.95rem; line-height: 1.4; margin: 0 0 0.7rem; }
h1 { font-size: 2.6rem; line-height: 1.1; margin: 0 0 0.7rem; color: var(--rosa-claro); }
/* div (no <p>) para evitar la regla del tema "h1 + p { opacity: .5 }" */
.subtitulo { font-size: 1.35rem; color: var(--rosa); margin: 0 0 1.8rem; }
.grupo { display: inline-block; background: var(--magenta); color: var(--rosa-claro);
         padding: 0.35rem 1rem; border-radius: 999px; font-weight: 700; font-size: 1rem; }
/* Completa dentro del marco: ni se corta a la derecha ni empieza de golpe a la izquierda */
.deco { position: absolute; right: 2rem; top: 50%; transform: translateY(-50%); width: 44%; }
</style>
