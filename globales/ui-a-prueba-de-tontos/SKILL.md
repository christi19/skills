---
name: ui-a-prueba-de-tontos
description: Crea y mejora interfaces web tan fáciles de usar que no requieren ningún conocimiento previo, que respetan la marca oficial de la empresa y que cargan rapidísimo desde el primer día (meta PageSpeed 100 en celular y escritorio). Usa este skill SIEMPRE que haya que crear o modificar cualquier interfaz visible — páginas, landings, formularios, dashboards, apps, pantallas de PWA, galerías o e-commerce — aunque el usuario no mencione "diseño" ni "velocidad". También cuando pida que algo se vea "profesional", "premium" o "moderno", que sea "fácil de usar" o "intuitivo", que cargue rápido o mejore en PageSpeed, cuando el público final sea gente no técnica, o cuando pida auditar, pulir, revisar u optimizar algo existente.
---

# UI a prueba de tontos, con la marca del cliente y carga rápida

Trabajá como un diseñador de producto senior que también es ingeniero de rendimiento. Cada pantalla tiene que cumplir tres cosas **a la vez, desde la primera línea de código**:

1. **Fácil:** la entiende cualquiera sin explicación.
2. **Fiel a la marca:** usa la identidad oficial de la empresa, no una inventada.
3. **Rápida:** carga casi al instante en un celular con señal regular.

No se construye primero y se optimiza después: eso obliga a rehacer. Cada componente nace usable, con la marca y liviano.

El público típico es gente real y ocupada: choferes, saloneros, floristas, electricistas, dueños de negocio. Usan más el celular que la computadora, con datos móviles, no leen manuales y abandonan a la primera frustración o a la primera página lenta.

## Criterio de aceptación

Ninguna pantalla está terminada hasta responder "sí" a las cuatro:

1. ¿Una persona de 12 años, o una abuela con celular, entiende qué hacer en los primeros 5 segundos sin que nadie le explique?
2. ¿Es imposible romper algo sin querer? (Toda acción destructiva se confirma o se puede deshacer.)
3. ¿Respeta el manual de marca de la empresa y se ve profesional?
4. ¿Carga rápido en celular? (Meta: PageSpeed 100; mínimo aceptable 90, y si no llega a 100, se explica por qué.)

Un "no" en cualquiera significa que falta trabajo. Respondé con honestidad.

## Elegí el modo

- **CREAR** (interfaz nueva) → "Flujo: crear".
- **MEJORAR** (interfaz existente) → "Flujo: auditar y mejorar". Nunca rediseñés en bloque: pasos pequeños, verificados y reversibles.

---

## Pilar 1 — A prueba de tontos

1. **Una acción principal por pantalla.** Un solo botón grande y obvio domina cada vista; lo secundario se ve secundario. Si hacen falta dos acciones principales, son dos pantallas.
2. **Lenguaje de persona, no de sistema.** "Guardar cambios", no "Submit"; "Fotos del trabajo", no "Adjuntos multimedia". Cero jerga técnica y cero anglicismos innecesarios. Vocabulario consistente: el botón "Publicar" produce el mensaje "Publicado".
3. **Trato al usuario: de usted por defecto** ("Toque el botón verde", "Escriba solo el número"). Si el proyecto ya usa otro trato (vos, tú) o el cliente lo pide, se respeta el del proyecto. Nunca mezclar tratos en la misma app.
4. **Dedos reales, no cursores.** Mobile-first. Objetivos táctiles de mínimo 48 px de alto y bien separados; texto base de 16–18 px (más si el público es mayor). Nada crítico depende de hover, gestos ocultos, doble clic ni menús contextuales.
5. **Respuesta inmediata a todo.** Cada toque responde en menos de 100 ms: estado presionado, "Guardando… → Guardado ✓". El silencio del sistema genera desconfianza y toques repetidos.
6. **Imposible de romper.** Lo destructivo se confirma describiendo la consecuencia concreta ("Se eliminará el gasto de ₡45.000. Esta acción no se puede deshacer."); ofrecé deshacer cuando se pueda; aceptá formatos variados ("8000", "8.000" y "₡8 000" son el mismo número). Mejor deshabilitar con explicación que dejar fallar.
7. **Estados vacíos que enseñan.** Una lista vacía dice qué es la sección, por qué está vacía y qué hacer, con el botón ahí mismo.
8. **Errores que dicen qué hacer.** Nunca códigos, culpas ni inglés: qué pasó y cómo resolverlo.
9. **Mostrá poco, revelá de a poco.** Lo que resuelve el 80 % de las tareas, visible; lo demás, detrás de "Más opciones".
10. **El camino siempre visible.** En flujos de varios pasos: "Paso 2 de 3" y una forma obvia de volver sin perder lo hecho.
11. **Bienvenida de máximo 3 pasos, siempre saltable.** Si hace falta más explicación, el problema es la interfaz.

## Pilar 2 — La marca del cliente

**Regla de oro: si la empresa tiene manual de marca, se usa el manual oficial.** Colores, tipografías, logo, tono y estilo de imágenes salen de ahí. No se "mejoran", no se reinterpretan y no se agregan colores ajenos.

1. **Antes de diseñar, buscá la identidad existente:** manual de marca (PDF, Figma, sistema de diseño), sitio actual, logo, redes sociales, o lo que diga el `AGENTS.md`/`CLAUDE.md` del proyecto. Si no la encontrás, preguntá.
2. **Si no existe manual:** proponé una paleta corta (fondo, texto, color principal, color de apoyo, éxito y peligro) y un par tipográfico **basados en el logo y el oficio del negocio**, y mostrásela a Christian **antes** de construir. Nunca la impongás en silencio ni copiés una paleta genérica.
3. **Un solo lugar para los colores y las fuentes.** Variables CSS (o tokens del sistema del proyecto) y nada de colores sueltos regados por los archivos. Si aparece un color fuera de los tokens, es deuda.
4. **Contraste legible:** mínimo AA. Si un color oficial no da contraste para texto, usalo en superficies grandes y avisá; no cambiés el color de marca por tu cuenta.

Acabado profesional, con la marca que sea:

- **El espacio en blanco es el lujo más barato.** Escala de espaciado consistente (múltiplos de 4/8 px) y aire alrededor de lo importante.
- **Profundidad suave:** sombras ligeras y radios coherentes en todo el sistema, no cajas grises con borde de 1 px por todas partes.
- **Cada elemento interactivo tiene sus estados:** normal, hover, presionado, foco visible, deshabilitado y cargando. Transiciones de 150–250 ms.
- **Contenido real desde el primer render:** nunca lorem ipsum ni "Título aquí".
- **Los detalles delatan la calidad:** skeletons al cargar, favicon, título de pestaña, imágenes bien recortadas, estados vacíos con ícono.
- **Antes de entregar, quitá un adorno.**

## Pilar 3 — Carga rápida desde el primer día

Meta: **PageSpeed 100 en celular y en escritorio.** Mínimo aceptable: 90 en celular. Si algo que el negocio necesita (analítica, mapa, chat, pasarela de pago) impide llegar a 100, se mantiene y se explica cuánto cuesta. Nunca se quita una función solo para subir un número, y nunca se hacen trampas a la medición.

Signos vitales que hay que cumplir (Core Web Vitals, medidos en celular):

| Medida | Qué es | Meta |
|---|---|---|
| LCP | Cuándo aparece lo principal | < 2,5 s (ideal < 1,8 s) |
| CLS | Cuánto "brinca" la página al cargar | < 0,1 (ideal 0) |
| INP | Cuánto tarda en responder a un toque | < 200 ms |

**Imágenes**
- Formatos livianos: AVIF o WebP, del tamaño en que se muestran (con `srcset`/`sizes` para celular y escritorio). Nunca una foto de 4000 px para mostrarla a 400.
- Siempre `width` y `height` (o `aspect-ratio`) para que la página no brinque.
- **Carga diferida** (`loading="lazy"` y `decoding="async"`) en todo lo que no se ve al abrir la página.
- La imagen principal de arriba (la del LCP) es la excepción: **sin lazy**, con `fetchpriority="high"` (o `priority` en `next/image`).
- Íconos en SVG, no en imágenes ni en fuentes de íconos completas.

**JavaScript**
- Lo mínimo al inicio. Código dividido por página o ruta; lo pesado (mapas, carruseles, editores, gráficos) se carga cuando hace falta (`import()` dinámico, carga al hacer scroll o al tocar).
- Lo que se puede hacer con HTML y CSS no se hace con JavaScript.
- Antes de agregar una librería, preguntate si hace falta. Preferí la nativa del navegador o una liviana.
- Terceros (analítica, chats, píxeles, mapas, videos embebidos) **nunca bloquean el primer render**: `async`/`defer`, carga después de que la página está lista o al primer toque. Los videos de YouTube se muestran como imagen y cargan el reproductor al tocar.

**Fuentes y CSS**
- Máximo 2 familias tipográficas y solo los pesos que se usan. Preferí servirlas desde el propio sitio (o `next/font`) con `font-display: swap`, y precargá solo la principal.
- CSS crítico primero; nada de hojas de estilo enormes que bloqueen el render. Purgá lo que no se usa.

**Servidor y caché**
- Compresión (Brotli/gzip) y caché larga para archivos con huella (`immutable`). Las plataformas como Cloudflare ya lo hacen; verificá que esté activo.
- Contenido que no cambia por usuario: generalo estático o en el borde cuando el framework lo permita.

**Medir siempre, no suponer**
- Antes y después de cada cambio importante: PageSpeed Insights sobre la URL publicada (o `npx lighthouse <url> --preset=perf` en modo celular para local o vista previa).
- Reportá los números reales de celular y escritorio, y si no llega a 100, qué lo impide y qué se podría hacer.

---

## Anti-patrones: si aparece uno, se corrige en el momento

- **Confunde:** dos acciones principales compitiendo · jerga técnica · íconos sin texto en acciones importantes · funciones escondidas en menús · errores en código o en inglés · formularios que pierden lo escrito · pantallas sin salida · cosas que dependen de hover en celular · tratos mezclados (usted y vos en la misma app).
- **Se ve poco profesional:** colores fuera del manual de marca · negro puro sobre blanco puro (salvo que la marca lo indique) · tres o más familias tipográficas · espaciados inconsistentes · botones sin estados · contenido de relleno · emojis como íconos en productos serios.
- **Pesa:** imágenes sin ancho y alto · fotos sin optimizar · carruseles o videos de fondo arriba de la página · librerías enteras para una sola función · scripts de terceros en el `<head>` sin `async`/`defer` · fuentes con todos los pesos · animaciones pesadas al cargar.

## Flujo: crear

1. **Conocé al usuario final:** quién es, en qué dispositivo trabaja, en qué contexto (¿en la calle, con una mano, con clientes esperando?) y su nivel digital. Si el brief no lo dice, declaralo con el mejor criterio y seguí.
2. **Conseguí la marca:** manual oficial o, si no existe, propuesta aprobada por Christian (Pilar 2). Definí los tokens (colores, fuentes, espaciado) en un solo lugar.
3. **Definí el presupuesto de velocidad:** qué es lo principal de cada página (LCP), qué terceros son indispensables y cómo se van a cargar sin bloquear.
4. **Boceteá la estructura:** una acción principal por pantalla y el camino feliz en el menor número de toques.
5. **Construí mobile-first desde los tokens.** Cada componente nace con sus estados, sus textos reales y sus imágenes optimizadas; nada se "arregla después".
6. **Medí** con PageSpeed en celular y escritorio, corregí y **pasá la prueba final**.

## Flujo: auditar y mejorar

1. **Recorré la interfaz como si fuera tu primer día:** hacé las 2–3 tareas principales del usuario real. Anotá cada duda de más de 2 segundos, cada texto que no entendería alguien sin estudios técnicos, cada color fuera de la marca.
2. **Medí la velocidad actual** con PageSpeed (celular y escritorio) y guardá los números de partida.
3. **Calificá** contra los tres pilares: cumple / no cumple / no aplica.
4. **Priorizá por impacto y riesgo:** primero lo que confunde en el flujo principal y lo que más pesa, después lo visual de alto impacto, de último lo cosmético.
5. **Mejorá una cosa a la vez.** Cada cambio se verifica por separado (compila, se ve bien, no rompe lo anterior y no empeora la velocidad). Los cambios visuales grandes o discutibles se proponen como opciones, no se imponen.
6. **Reportá:** qué mejoró, números de PageSpeed antes y después, qué quedó pendiente y cuál sería la siguiente mejora.

## Recetas rápidas por stack

- **Next.js:** `next/image` con `width`/`height` y `sizes`; `priority` solo en la imagen principal; `next/font` para las fuentes; `next/dynamic` para componentes pesados; `next/script` con `strategy="lazyOnload"` para terceros. Diseñá `loading.tsx`, `error.tsx` y `not-found.tsx`: el usuario también los ve.
- **React + Vite:** `<img>` con `srcset`, `sizes`, `width`, `height`, `loading="lazy"`; `React.lazy` + `Suspense` por ruta; `<link rel="preload">` para la imagen principal y la fuente principal; revisá el tamaño del paquete en cada build (si un archivo de JavaScript pasa de ~200 kB comprimido, dividilo).
- **Tailwind:** colores y fuentes del manual mapeados como tokens (`@theme` en v4 o `theme.extend` en v3); en los `className` solo clases semánticas (`bg-marca`, `text-tinta`), nunca códigos de color sueltos. `min-h-12` en todo lo tocable, `focus-visible:` en todo lo interactivo y `motion-reduce:` en toda animación.
- **HTML/CSS sin framework:** variables CSS en `:root` para la marca, imágenes con `srcset` y lazy, scripts con `defer`.
- Si el proyecto trae un archivo `references/react-tailwind.md` con una paleta o fuentes de ejemplo (crema, terracota, Fraunces), **ignorá esos colores y fuentes**: quedaron obsoletos. Mandan la marca del cliente y este documento.

## Prueba final antes de entregar

- ¿Pasa las cuatro preguntas del criterio de aceptación?
- ¿Cada pantalla tiene UNA acción principal evidente?
- ¿Todos los textos están en el idioma y el trato del usuario final, sin jerga?
- ¿Colores, fuentes y logo salen del manual de marca (o de la propuesta aprobada)?
- ¿Todo elemento interactivo tiene sus estados completos, incluido foco visible?
- ¿Se ve bien a 360 px de ancho y en escritorio?
- ¿Existen estados vacíos, de carga y de error diseñados a propósito?
- ¿Contraste mínimo AA y se respeta `prefers-reduced-motion`?
- ¿Todas las imágenes tienen formato liviano, ancho y alto, y carga diferida (menos la principal)?
- ¿Ningún script de terceros bloquea el primer render?
- ¿PageSpeed en celular y escritorio medido y reportado con números reales? ¿100, o explicado por qué no?
- ¿Ya quitaste un adorno?
