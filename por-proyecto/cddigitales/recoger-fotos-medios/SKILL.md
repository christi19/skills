---
name: recoger-fotos-medios
description: Recoge las fotos de una carpeta del panel de medios de CD Digitales (medios.cddigitales.com), mira y analiza cada una, y las coloca en el sitio web que se está construyendo con los enlaces de Backblaze B2, con textos alternativos, títulos, descripciones y textos de venta escritos a partir de lo que se ve en cada foto. Sirve para galerías, aparadores y catálogos de cualquier producto (pasteles, carros, flores, ropa…). Usala cuando Christian diga "recogé las fotos de tal carpeta", pegue un enlace de medios.cddigitales.com/panel o una lista de enlaces de B2, o pida armar una galería con fotos que ya subió al panel.
---

# Recoger fotos del panel de medios

Christian sube las fotos al panel (medios.cddigitales.com), en un proyecto y una carpeta, y te dice dónde están y qué hacer con ellas. Vos:

1. traés el enlace de cada foto,
2. **mirás y analizás cada foto** (no te quedés con el nombre del archivo),
3. escribís sus textos a partir de lo que viste,
4. las colocás en el sitio con **los enlaces de B2 tal cual**.

No copiás las fotos dentro del proyecto ni las volvés a subir a ningún lado: el sitio las muestra desde el enlace.

**Requisito:** tenés que poder ver imágenes. Si tu modelo no puede, decíselo a Christian y pará; este trabajo no se puede hacer a ciegas.

**Versión oficial:** https://github.com/christi19/skills (`por-proyecto/cddigitales/recoger-fotos-medios/SKILL.md`). Si tenés una copia y no coincide con la del repositorio, manda la del repositorio.

## 1. Entender el pedido

Necesitás cuatro datos. Si falta alguno, preguntá antes de empezar:

| Dato | Ejemplo |
|---|---|
| **Dónde están las fotos** | `https://medios.cddigitales.com/panel/pasteleria-dulce?carpeta=2026-10-30-pasteles` |
| **Qué negocio y qué vende** | "Pastelería en Siquirres, queques por encargo" |
| **Qué hay que hacer** | "Galería tipo aparador con descripción corta y texto persuasivo en cada una" |
| **En qué sitio y en qué parte** | "En la página /catalogo del sitio que estamos construyendo" |

En el enlace del panel, lo que va después de `/panel/` es el **proyecto** y lo que va después de `carpeta=` es la **carpeta**.

## 2. Traer los enlaces

**Camino A — con el comando `medios`** (agentes en la PC de Christian):

```
medios listar --proyecto <proyecto> --carpeta <carpeta> --limite 500
```

Si `medios` no está en el PATH:

```
node "C:\Users\ctr04\Projects\Ecosistema cddigitales\02-panel-medios\cdd-medios\cli\medios.mjs" listar --proyecto <proyecto> --carpeta <carpeta> --limite 500
```

Devuelve un JSON con `total` e `items`; de cada foto usá `url`, `ancho` y `alto` tal como vienen. Si `total` es mayor que la cantidad de `items`, subí el `--limite`. Si la lista viene vacía, revisá que la carpeta esté bien escrita (minúsculas, guiones, sin tildes) y avisale a Christian. Las credenciales están en `C:\Users\ctr04\.cdd-medios.env`: **nunca las mostrés, copiés ni leás en voz alta**. Si el comando termina con código 2 (sin acceso), pasá al camino B.

**Camino B — sin el comando** (cualquier otro agente o dispositivo): pedile a Christian que abra la carpeta en el panel, marque las fotos y toque **«Copiar URLs»** en la barra de abajo, y que te pegue la lista. Cada línea es un enlace público. El ancho y el alto los sacás al descargar cada foto. (Hoy las fotos se marcan una por una; con muchas fotos, el camino A es más rápido.)

Antes de seguir, confirmale a Christian cuántas fotos encontraste ("Encontré 80 fotos en 2026-10-30-pasteles"). Si el número no le cuadra, se detiene ahí.

**Nunca armés un enlace a mano ni le cambiés nada.** Si un enlace no abre, anotalo y seguí con los demás.

## 3. Ver y analizar cada foto

Descargá las fotos a una carpeta temporal **fuera del proyecto** y miralas **en tandas de 10**, para no saturarte con muchas imágenes juntas. Por cada foto llená una ficha y guardalas todas en un archivo de trabajo (`fichas-fotos.json` en la carpeta temporal). Así no se pierde nada aunque la sesión se corte, y podés retomar desde la última ficha.

```json
{
  "url": "https://…/pasteles-boda-3f9a1c.webp",
  "ancho": 1600, "alto": 1200,
  "que_se_ve": "Queque de dos pisos, cubierta blanca, flores de azúcar rosadas, base dorada",
  "tipo": "boda",
  "detalles_visibles": ["dos pisos", "flores de azúcar", "cubierta lisa blanca"],
  "dudas": "No se distingue el sabor del relleno",
  "calidad": "buena"
}
```

Mientras analizás:

- **Agrupá** por tipo (en pasteles: cumpleaños, boda, infantiles, cupcakes…; en carros: marca, modelo, color) para ordenar la galería.
- **Marcá las fotos con problemas**: borrosas, oscuras, repetidas o que no son del tema. No las usés sin preguntar.
- **Regla de honestidad:** escribí solo lo que se ve. Una marca o un modelo, solo si se distingue claramente (logo, emblema, forma inconfundible). Sabores, ingredientes, tamaños en porciones, precios, año, motor, kilometraje o garantía **no se inventan**: si hacen falta, pedíselos a Christian. Un texto de venta con datos falsos le hace daño al negocio.

## 4. Escribir los textos

En español claro de Costa Rica, sin jerga técnica ni palabras repetidas para "posicionar".

| Texto | Para qué sirve | Largo |
|---|---|---|
| `alt` | Describe la foto para quien no la ve y para Google | 8–20 palabras, concreto |
| Título | Nombre corto de la pieza ("Queque de boda de dos pisos") | 3–8 palabras |
| Descripción | Lo que tiene, a partir de lo que se ve | 1–2 oraciones |
| Texto persuasivo (si se pide) | Invita a comprar o encargar, conectado con una ocasión real | 1 oración, sin exagerar |
| Meta descripción | Solo para una página nueva o la página de la galería | 140–160 caracteres |

Que los textos no salgan todos iguales: variá el comienzo y el ángulo (la ocasión, el detalle que destaca, a quién le gustaría).

**Antes de escribir las 80, mostrale a Christian una muestra de 5** con todos sus textos. Si aprueba el tono, seguís con el resto; si corrige, ajustás el estilo. Al terminar, mostrale la tabla completa (foto → título → alt → descripción → texto persuasivo) **antes** de tocar el sitio.

## 5. Colocar en el sitio

1. Leé primero cómo el sitio maneja sus imágenes y su contenido (`AGENTS.md`/`CLAUDE.md`, componentes, archivos de datos) y seguí ese patrón.
2. Para muchas fotos, poné los datos en un archivo de contenido (por ejemplo `src/content/galeria-pasteles.js` o `.json`) y armá la galería desde ahí. No escribás 80 bloques a mano en la página.
3. Cada foto lleva: el enlace de B2 tal cual, `width` y `height`, el `alt` aprobado, `loading="lazy"` (menos las primeras visibles) y `decoding="async"`.
4. La galería tiene que verse bien en celular, ordenada por los grupos del paso 3. Si el sitio ya tiene un componente de galería, usalo.
5. Si el sitio bloquea imágenes externas (lista de dominios permitidos de Next.js, política de seguridad), avisale a Christian antes de tocar esa configuración.
6. Hacé un commit antes de editar. Después verificá que compile sin errores y que la página muestre todas las fotos.
7. **No publiqués** hasta que Christian lo pida.

## 6. Reportar

- Cuántas fotos recogiste, cuántas usaste y dónde quedaron.
- Las que no usaste y por qué (borrosas, repetidas, fuera de tema, enlace roto).
- Las dudas que quedaron abiertas (datos que Christian tiene que dar).

## Lo que esta skill NO hace

- No borra, mueve ni renombra fotos del panel.
- No cambia títulos ni textos dentro del panel.
- No sube fotos nuevas. Si Christian te pasa fotos sueltas, primero se suben desde el panel o con `medios subir`.
