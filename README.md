# Skills de Christian

Instrucciones reutilizables para agentes de IA (Claude, Codex, Gemini, DeepSeek…). Cada skill es una carpeta con un `SKILL.md`: arriba trae su nombre y cuándo usarla, y abajo, el paso a paso.

**Cómo usar una skill con cualquier agente:** pasale el enlace del `SKILL.md` y decile qué hacer. Por ejemplo:

> Leé https://raw.githubusercontent.com/christi19/skills/main/por-proyecto/cddigitales/recoger-fotos-medios/SKILL.md y seguilo. Las fotos están en https://medios.cddigitales.com/panel/pasteleria?carpeta=2026-10-30-pasteles. Armá una galería tipo aparador en la página /catalogo, con descripción y texto persuasivo en cada foto.

## Índice

| Skill | Qué hace | Se usa en |
|---|---|---|
| [recoger-fotos-medios](por-proyecto/cddigitales/recoger-fotos-medios/SKILL.md) | Recoge las fotos de una carpeta del panel medios.cddigitales.com, las mira una por una y las coloca en un sitio (galerías, aparadores, catálogos) con los enlaces de B2 y textos escritos a partir de lo que se ve | Cualquier sitio que use fotos del panel de CD Digitales |
| [ui-a-prueba-de-tontos](globales/ui-a-prueba-de-tontos/SKILL.md) | Crea y mejora interfaces web que entiende cualquiera sin explicación, fieles a la marca oficial del cliente y con carga rápida desde la primera línea (meta PageSpeed 100 en celular y escritorio) | Cualquier interfaz visible: páginas, landings, formularios, dashboards, apps, PWAs, galerías, e-commerce |

## Reglas del repositorio

- **Este repo es la versión oficial.** Si una skill cambia, se cambia aquí primero y después se actualiza en Claude.
- **Es público: nunca lleva claves, contraseñas ni tokens.** Una skill puede nombrar un archivo de credenciales, pero jamás copiar su contenido.
- `globales/` = skills para cualquier proyecto. `por-proyecto/<proyecto>/` = skills que se cargan solo en ese proyecto.
- Al agregar una skill, se agrega su fila al índice.
