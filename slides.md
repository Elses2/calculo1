---
theme: default
title: TP N°7 · Análisis de Funciones · Grupo 4
colorSchema: dark
mdc: true
transition: fade
fonts:
  sans: Lato
  mono: Fira Code
layout: portada
materia: Cálculo I · UNVIME · Bioingeniería / Ing. en Sistemas de la Información
titulo: Análisis de funciones
subtitulo: Trabajo Práctico N°7
grupo: Grupo 4
---

<!--
TIEMPOS (20 min): portada 0:20 · marco teórico 2:00 · Ej.1 6:00 · Ej.2 3:30 · Ej.3 6:00 · cierre 0:40 · margen 1:30
Presentar: nombre del grupo y qué vamos a mostrar (3 ejercicios, siempre citando el apunte).
-->

---
layout: seccion
numero: 0
---

# Marco teórico
Tres ideas del apunte que usamos en todo el TP.

---
layout: default
---

# Las tres ideas clave

<Caja tipo="definicion" apunte="7.3">

$c$ es **punto crítico** de $f$ si $f$ está definida en $c$ y $f'(c)=0$ o $f'(c)$ no existe.

</Caja>

<Caja tipo="teorema" apunte="Teorema 2">

Si $f'$ cambia de signo en un punto crítico $c$, hay un **extremo relativo** en $c$.

</Caja>

<Caja tipo="definicion" titulo="Punto de inflexión" apunte="7.6">

$f$ continua en $c$ y **cambia de concavidad** en $c$.

</Caja>

<!--
[~40 s] Leer las tres cajas. Remarcar: "f definida en c" es parte de la definición (lo vamos a usar en 3.c).
-->

---
layout: video
titulo: "Punto crítico: tres casos"
video: /videos/C02_PuntoCritico.mp4
apunte: 7.3
---

- $f'(c)=0$: tangente horizontal
- $f'(c)$ no existe: punta o pico
- Si $c\notin\mathrm{Dom}f$ **no** es punto crítico

<!-- [~40 s] Mostrar x², |x| y 1/x. -->

---
layout: video
titulo: "Concavidad y recta tangente"
video: /videos/C04_Concavidad.mp4
apunte: 7.5
---

- Curva **sobre** la tangente: cóncava ↑, $f''>0$
- Curva **bajo** la tangente: cóncava ↓, $f''<0$

<!-- [~30 s] -->

---
layout: video
titulo: "Punto de inflexión"
video: /videos/C05_Inflexion.mp4
apunte: 7.6 · 7.7
---

- La tangente **atraviesa** la curva
- Cambia el signo de $f''$
- $f''(c)=0$ **no alcanza**

<!-- [~30 s] Adelantar que 3.e y 3.h usan esta idea. -->

---
layout: seccion
numero: 1
---

# Análisis completo de funciones
Dominio, paridad, cortes, asíntotas, críticos, inflexión, crecimiento y concavidad.

---
layout: video
titulo: "1.a · y = x²·e^(−x²) · estructura"
video: /videos/E1a_Estructura.mp4
---

- $\mathrm{Dom}f=\mathbb{R}$ · **par**: $f(-x)=f(x)$
- Corte único: $(0,0)$
- Asíntota horizontal $y=0$; sin verticales

<!-- [~40 s] Ojo: el factor es x², no x (no confundir con el ejemplo del apunte). -->

---
layout: video
titulo: "1.a · críticos e inflexión"
video: /videos/E1a_Derivadas.mp4
apunte: 7.3 · Teorema 2 · 7.6
---

- $f'=2x\,e^{-x^2}(1-x^2)$
- $x=0$: <span class="f1">mín. rel.</span> · $x=\pm1$: <span class="f1">máx. rel.</span>, $f=1/e$
- <span class="f2">4 inflexiones</span>: $x\approx\pm0{,}47$ y $\pm1{,}51$

<!-- [~40 s] -->

---
layout: video
titulo: "1.a · gráfico final"
video: /videos/E1a_Grafico.mp4
---

- Crece en $(-\infty,-1)\cup(0,1)$
- Decrece en $(-1,0)\cup(1,\infty)$

<!-- [~25 s] -->

---
layout: video
titulo: "1.b · y = x³ − 3x² · estructura"
video: /videos/E1b_Estructura.mp4
---

- $\mathrm{Dom}f=\mathbb{R}$ · ni par ni impar
- Cortes: $(0,0)$ y $(3,0)$
- Sin asíntotas

<!-- [~35 s] -->

---
layout: video
titulo: "1.b · críticos e inflexión"
video: /videos/E1b_Derivadas.mp4
apunte: 7.3 · Teorema 2 · 7.6
---

- $f'=3x(x-2)$
- $x=0$: <span class="f1">máx. rel.</span> · $x=2$: <span class="f1">mín. rel.</span>
- <span class="f2">Inflexión</span> en $(1,-2)$

<!-- [~35 s] -->

---
layout: video
titulo: "1.b · gráfico final"
video: /videos/E1b_Grafico.mp4
---

- Crece en $(-\infty,0)\cup(2,\infty)$
- Cóncava ↓ en $(-\infty,1)$, cóncava ↑ en $(1,\infty)$

<!-- [~25 s] -->

---
layout: video
titulo: "1.c · y = x − 1/x · estructura"
video: /videos/E1c_Estructura.mp4
---

- $\mathrm{Dom}f=\mathbb{R}\setminus\{0\}$ · **impar**
- Cortes: $(\pm1,0)$; no corta el eje $y$
- Asíntotas: vertical $x=0$ y oblicua $y=x$

<!-- [~40 s] -->

---
layout: video
titulo: "1.c · derivadas"
video: /videos/E1c_Derivadas.mp4
apunte: 7.3 · 7.6
---

- $f'=1+\dfrac{1}{x^2}>0$: **sin puntos críticos**
- $f'$ no existe en $0$, pero $0\notin\mathrm{Dom}f$
- $f''=-\dfrac{2}{x^3}$

<!-- [~35 s] Conectar con la definición de 7.3 (c debe estar en el dominio). -->

---
layout: video
titulo: "1.c · gráfico final"
video: /videos/E1c_Grafico.mp4
---

- Crece en $(-\infty,0)$ y en $(0,\infty)$
- Cóncava ↑ en $(-\infty,0)$, ↓ en $(0,\infty)$
- **Sin inflexión**: el cambio ocurre en $0\notin\mathrm{Dom}f$

<!-- [~30 s] -->

---
layout: seccion
numero: 2
---

# Fenómeno real: usuarios activos
$A(t)=\dfrac{200}{1+e^{-0{,}4\,(t-12)}}$, en miles, con $t$ en meses.

---
layout: video
titulo: "2.a · ¿Hay puntos críticos?"
video: /videos/E2a_SinCriticos.mp4
apunte: 7.3 · Teorema 1
---

- $A'(t)=\dfrac{L\,r\,e^{-r(t-t_0)}}{\left(1+e^{-r(t-t_0)}\right)^2}>0$
- **Ningún** punto crítico: $A'$ nunca se anula
- $A$ estrictamente creciente

<!-- [~45 s] -->

---
layout: video
titulo: "2.b · concavidad e inflexión"
video: /videos/E2b_Inflexion.mp4
apunte: 7.6 · 7.7
---

- Cóncava ↑ si $t<12$, cóncava ↓ si $t>12$
- Inflexión en $t_0=12$: $A(t_0)=100$
- $A'(t_0)=20$ mil usuarios por mes

<!-- [~50 s] -->

---
layout: video
titulo: "2.c · ¿qué cambia en t₀?"
video: /videos/E2c_Colega.mp4
apunte: 7.3 · 7.6
---

- $A'(12)=20\neq0$: **no** es punto crítico
- Cambia la concavidad, no el signo de $A'$
- Crece cada vez más rápido, luego cada vez más lento

<!-- [~45 s] Responder al colega: "cambia de forma" no es la definición de 7.3. -->

---
layout: video
titulo: "2.d · el gerente y el valor de L"
video: /videos/E2d_Gerente_L.mp4
---

- El crecimiento empieza a frenarse en $t_0=12$ meses
- $L=200$: capacidad del mercado (asíntota $y=200$)
- Después de $t_0$, cada mes suma menos usuarios

<!-- [~50 s] -->

---
layout: seccion
numero: 3
---

# Verdadero o falso
Cada respuesta se justifica con el apunte y un ejemplo.

---
layout: afirmacion
id: '3.a'
veredicto: F
apunte: 7.3 · Teorema 2
video: /videos/E3a_Cubica.mp4
---

::enunciado::
Si $f'(c)=0$, entonces $f$ tiene un máximo o un mínimo relativo en $c$.

::default::
<Caja tipo="contraejemplo">

$f(x)=x^3$, $c=0$: $f'(0)=0$, pero $f'$ **no cambia de signo**. Falla la hipótesis del Teorema 2.

</Caja>

<!-- [~40 s] -->

---
layout: afirmacion
id: '3.b'
veredicto: F
apunte: 7.3
video: /videos/E3b_Pico.mp4
---

::enunciado::
Si $f$ tiene un máximo relativo en $c$, entonces $f'(c)=0$.

::default::
<Caja tipo="contraejemplo">

$f(x)=-|x|$, $c=0$: máximo relativo, pero $f'(0)$ **no existe**. El extremo puede estar donde $f'$ no existe.

</Caja>

<!-- [~35 s] -->

---
layout: afirmacion
id: '3.c'
veredicto: F
apunte: 7.3 (definición de punto crítico)
video: /videos/E3c_NoDominio.mp4
---

::enunciado::
Si $f'$ no está definida en $c$, entonces $c$ es un punto crítico de $f$.

::default::
<Caja tipo="contraejemplo">

$f(x)=1/x$, $c=0$: $f'$ no está definida, pero $0\notin\mathrm{Dom}f$. La definición exige $f$ definida en $c$.

</Caja>

<!-- [~40 s] -->

---
layout: afirmacion
id: '3.d'
veredicto: F
apunte: 7.1 · Teorema 1
video: /videos/E3d_FPrimaCero.mp4
---

::enunciado::
Si $f$ es estrictamente creciente en $(a,b)$, entonces $f'(x)>0$ para todo $x$ de $(a,b)$.

::default::
<Caja tipo="contraejemplo">

$f(x)=x^3$ en $(-1,1)$: estrictamente creciente, pero $f'(0)=0$. El Teorema 1 vale en un solo sentido: creciente implica $f'\ge0$.

</Caja>

<!-- [~40 s] -->

---
layout: afirmacion
id: '3.e'
veredicto: F
apunte: 7.6 · 7.7
video: /videos/E3e_Cuartica.mp4
---

::enunciado::
Si $f''(c)=0$, entonces $(c,f(c))$ es un punto de inflexión.

::default::
<Caja tipo="contraejemplo">

$f(x)=x^4$, $c=0$: $f''(0)=0$, pero es cóncava ↑ a ambos lados. **No hay cambio de concavidad**.

</Caja>

<!-- [~35 s] -->

---
layout: afirmacion
id: '3.f'
veredicto: F
apunte: 7.1 · 7.5
video: /videos/E3f_Descendente.mp4
---

::enunciado::
Si $f$ es cóncava hacia arriba en un intervalo, entonces $f$ es creciente en ese intervalo.

::default::
<Caja tipo="contraejemplo">

$f(x)=x^2$ en $(-\infty,0)$: cóncava ↑ y **decreciente**. Concavidad ($f''$) y crecimiento ($f'$) son distintos.

</Caja>

<!-- [~35 s] -->

---
layout: afirmacion
id: '3.g'
veredicto: V
apunte: Criterio de la 2.ª derivada · Teorema 2
video: /videos/E3g_SegundaDerivada.mp4
---

::enunciado::
Si $f'(c)=0$ y $f''(c)>0$, entonces $f$ tiene un mínimo relativo en $c$.

::default::
<Caja tipo="nota" titulo="Por qué es verdadera">

$f''(c)>0$ dice que $f'$ tiene pendiente positiva en $c$, y $f'(c)=0$: entonces $f'<0$ a la izquierda y $f'>0$ a la derecha. Por el Teorema 2, mínimo relativo.

</Caja>

<!--
[~45 s] El apunte enuncia el criterio con f''>0 en un intervalo; acá se llega igual mirando f' cerca de c.
Confirmar con la cátedra cómo esperan esta respuesta.
-->

---
layout: afirmacion
id: '3.h'
apunte: Criterio de la 2.ª derivada · Teorema 2 · 7.6
video: /videos/E3h_TresCasos.mp4
---

::enunciado::
Con $x^3$, $x^4$ y $-x^4$ en $c=0$: $f''(0)=0$ en las tres. ¿Qué pasa en cada una?

::default::
<Caja tipo="nota" titulo="Tres situaciones distintas">

- $x^3$: <span class="f2">inflexión</span>
- $x^4$: <span class="f1">mínimo relativo</span>
- $-x^4$: <span class="f1">máximo relativo</span>

Se decide con el **signo de $f'$** a cada lado (Teorema 2) y de $f''$ (7.6).

</Caja>

<!-- [~50 s] Cierra el Ejercicio 3: f''=0 nunca decide por sí solo. -->

---
layout: default
---

# Conclusiones

- **Punto crítico**: $c\in\mathrm{Dom}f$ y ($f'(c)=0$ o $f'(c)$ no existe)
- Crecimiento, extremos y concavidad son **tres cosas distintas**
- $f'(c)=0$ y $f''(c)=0$ **no deciden**: hay que mirar el cambio de signo

<div class="muted" style="margin-top:2rem">Gracias · ¿Preguntas?</div>

<!-- [~40 s] Quedan ~1:30 de margen para preguntas. -->
