# Bono: Agentes de IA

Este repositorio contiene 4 agentes de inteligencia artificial listos para usar con **Claude Code**. Son "skills": instrucciones detalladas que convierten a Claude en un especialista en una tarea puntual, entrenado con tu criterio y tu información de negocio (no con conocimiento genérico de internet).

No son herramientas para webinars ni para ningún nicho en particular — sirven para cualquier negocio que venda por Instagram, ya sea con lanzamientos puntuales o con contenido evergreen (de todos los días, sin fecha de vencimiento).

## Qué incluye

| Agente | Qué hace |
|---|---|
| [`optimizacion-de-perfil`](skills/optimizacion-de-perfil/SKILL.md) | Te entrega tu bio, tus destacadas, tus posts fijados y tu estética de Instagram — todo pensado para que el perfil venda solo. |
| [`guionista-de-reels`](skills/guionista-de-reels/SKILL.md) | Te escribe el guion completo de un reel, a partir de una referencia que ya funcionó, con tu mensaje y tu voz. |
| [`arquitecto-de-oferta`](skills/arquitecto-de-oferta/SKILL.md) | Te ayuda a poner tu oferta en una sola frase clara (y la baja a tu bio de Instagram). |
| [`crear-agente`](skills/crear-agente/SKILL.md) | Un agente que crea OTROS agentes: te entrevista sobre cualquier tarea que repitas seguido y te entrega una skill nueva, lista para usar. |

## Cómo empezar

1. Instala Claude Code (si todavía no lo tienes) y copia estas 4 skills a tu computadora — paso a paso en [`INSTALACION.md`](INSTALACION.md).
2. Antes de usar un agente por primera vez, abre su archivo `SKILL.md` y completa la sección **[COMPLETÁ ESTO]** con los datos de tu negocio (o pégaselos a Claude directamente al pedirle que use el agente — te los va a pedir si faltan).
3. Listo: pídele a Claude lo que necesites (ej. "optimizame el perfil de Instagram" o "escribime un reel") y el agente correspondiente se activa solo.

## Cómo funcionan (lo mínimo que necesitas saber)

- Cada agente vive en su propia carpeta dentro de `skills/`, con un único archivo `SKILL.md` adentro.
- Claude Code detecta automáticamente cuál skill usar según lo que le pidas — no necesitas invocarlas con un comando especial, aunque también podés escribir `/optimizacion-de-perfil`, `/guionista-de-reels`, etc. si querés ser explícito.
- Ningún agente inventa información: si le falta un dato de tu negocio, te lo va a preguntar antes de entregarte algo.
- Podés editar cualquier `SKILL.md` con un editor de texto simple para ajustar el tono, agregar reglas propias, o completar tus datos de forma permanente.
