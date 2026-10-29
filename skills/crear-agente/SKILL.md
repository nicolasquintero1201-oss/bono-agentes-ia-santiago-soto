---
name: crear-agente
description: Crear un agente especializado (una skill de Claude Code) mediante una entrevista profunda. El agente hace TODAS las preguntas necesarias para construir una skill completa a partir de tu conocimiento. Activar cuando el usuario diga crear agente, nuevo agente, quiero un agente para X, o /crear-agente.
argument-hint: "[nombre-del-agente]"
---

# Crear Agente — Entrevista Profunda

## Propósito
Construir agentes especializados (skills de Claude Code) para cualquier proceso que el usuario repita seguido. Cada agente se crea a través de una entrevista donde el usuario carga toda la información, criterio y conocimiento. El agente NUNCA inventa — todo sale de lo que el usuario dice.

## Flujo completo

### FASE 1: Contexto inicial
Preguntar:
1. Nombre del agente — "¿Cómo se llama esta funcionalidad? (ej: creador-de-emails, analizador-de-llamadas)"
2. Qué hace — "Explícame en tus palabras qué tiene que hacer este agente. Como si se lo explicaras a un empleado nuevo."
3. Para quién — "¿Quién va a usar este agente? Tú, tu equipo, o un cliente directo?"
4. Input típico — "¿Qué le vas a pasar al agente? (ej: transcript, brief, descripción, captura de pantalla)"
5. Output esperado — "¿Qué tiene que entregar? Descríbeme el output ideal."

### FASE 2: El conocimiento (la más importante)
6. Tu proceso — "Si tú hicieras esto a mano, ¿cuáles son los pasos exactos? Enuméralos."
7. Criterio de calidad — "¿Cómo distingues un output bueno de uno malo? Dame ejemplos concretos."
8. Errores comunes — "¿Qué errores se cometen frecuentemente al hacer esto? ¿Qué NO debería hacer el agente?"
9. Frameworks o estructuras — "¿Tienes algún framework, plantilla, o estructura que uses? Si sí, pásala."
10. Ejemplos reales — "¿Tienes un ejemplo de un output que consideres 10/10? Pásalo."
11. Variaciones — "¿Hay distintos tipos o variaciones de este output?"
12. Dependencias — "¿Este agente necesita información de otro agente o proceso previo?"

### FASE 3: Personalización
13. Datos que necesita — "¿Qué datos tuyos o de tu cliente necesita el agente para personalizar el output?"
14. Tono — "¿En qué tono tiene que hablar/escribir? ¿Hay algo que NUNCA debería decir?"

### FASE 4: Iteración
15. ¿Algo más? — "¿Hay algo que no te pregunté y que es importante para que este agente sea épico?"

Después de cada respuesta, si es vaga o incompleta, REPREGUNTAR con ejemplos concretos. No avanzar hasta tener una respuesta sólida. Si el usuario dice "no sé" o "lo que tú creas", insistir: "Necesito tu criterio real. Si no me lo das, el agente va a inventar y no va a ser bueno."

## Qué se genera al final

Una skill de Claude Code lista para usar, en formato `SKILL.md`, con esta estructura:

```
---
name: [nombre-del-agente]
description: "[una frase que explica qué hace y cuándo se activa]"
---

# Rol
[En 1 párrafo: qué es este agente y para qué sirve]

# Datos que necesita [COMPLETÁ ESTO]
[Los datos de personalización de la FASE 3, como preguntas a completar]

# Proceso
[Los pasos exactos de la FASE 2, en orden]

# Formato de output
[Cómo tiene que entregar el resultado]

# Reglas
[Los anti-patrones de la FASE 2: lo que NUNCA debe hacer, los errores comunes a evitar]
```

Al terminar, explicar en una línea dónde guardar el archivo: dentro de una carpeta con el nombre del agente en `.claude/skills/` (del proyecto) o en `~/.claude/skills/` (para que esté disponible en cualquier proyecto), siempre como `SKILL.md`.

## Reglas de la entrevista
- NUNCA saltear preguntas
- NUNCA asumir respuestas — todo sale del usuario
- Si las respuestas son largas, resumir y confirmar: "Entendí que [X]. ¿Está bien?"
- Preguntar de a una o dos, no tirar las 15 de golpe
- Al final, mostrar un preview del agente antes de guardarlo
- Hablar en el idioma y tono que use el usuario (por defecto, español neutro con "tú")
