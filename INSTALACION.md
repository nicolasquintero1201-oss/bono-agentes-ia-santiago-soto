# Instalación — paso a paso

No necesitas saber programar para hacer esto. Son 4 pasos, se hacen una sola vez.

## Paso 1 — Instalar Claude Code

Claude Code es la herramienta de Anthropic que va a correr estos agentes. Es gratis instalarla (se paga por uso, como cualquier herramienta de IA).

1. Instala [Node.js](https://nodejs.org) si no lo tienes (es un requisito técnico de Claude Code — bajalo e instalalo como cualquier programa, con las opciones por defecto).
2. Abre una terminal:
   - **Windows:** buscá "PowerShell" en el menú de inicio.
   - **Mac:** abrí la app "Terminal" (buscala con Cmd+Espacio).
3. Pegá este comando y presioná Enter:

   ```bash
   npm install -g @anthropic-ai/claude-code
   ```

4. Cuando termine, escribí `claude` y presioná Enter. Te va a pedir iniciar sesión con tu cuenta de Anthropic/Claude (si no tenés, la creás ahí mismo).

Si algo de esto falla, la guía oficial y siempre actualizada está en **https://docs.claude.com/claude-code**.

## Paso 2 — Descargar estos agentes

**Opción fácil (sin usar git):** en la página de este repositorio en GitHub, hacé clic en el botón verde **"Code"** → **"Download ZIP"**, y descomprimilo en tu computadora.

**Opción con git** (si ya lo usás):

```bash
git clone <URL-de-este-repositorio>
```

## Paso 3 — Copiar las skills a Claude Code

Claude Code busca las skills en una carpeta llamada `.claude/skills` dentro de tu carpeta de usuario (así están disponibles en cualquier proyecto que abras, no solo en uno).

1. Localizá tu carpeta de usuario:
   - **Windows:** `C:\Users\TU-NOMBRE\`
   - **Mac:** `/Users/TU-NOMBRE/`
2. Dentro, buscá o creá la carpeta `.claude\skills` (Windows) o `.claude/skills` (Mac). Si no existe, creala.
   - En Windows, si el Explorador no te deja crear una carpeta que empiece con un punto, abrí PowerShell en esa ubicación y corré: `mkdir .claude\skills`
3. Copiá dentro de esa carpeta las 4 subcarpetas que están en `skills/` de este repositorio (`optimizacion-de-perfil`, `guionista-de-reels`, `arquitecto-de-oferta`, `crear-agente`), cada una con su `SKILL.md` adentro.

Al final tenés que tener algo así:

```
C:\Users\TU-NOMBRE\.claude\skills\optimizacion-de-perfil\SKILL.md
C:\Users\TU-NOMBRE\.claude\skills\guionista-de-reels\SKILL.md
C:\Users\TU-NOMBRE\.claude\skills\arquitecto-de-oferta\SKILL.md
C:\Users\TU-NOMBRE\.claude\skills\crear-agente\SKILL.md
```

## Paso 4 — Usarlos

1. Abrí una terminal en cualquier carpeta y escribí `claude` para iniciar una sesión.
2. Pedile lo que necesites en lenguaje natural, por ejemplo:
   - "Ayudame a optimizar mi perfil de Instagram"
   - "Escribime un reel de este estilo: [pegás un link o transcript]"
   - "Necesito definir mi oferta"
   - "Quiero crear un agente para [tu tarea repetitiva]"
3. Claude va a activar la skill correspondiente sola. La primera vez te va a pedir los datos de tu negocio que falten (nicho, avatar, oferta, etc.) — respondéselos una vez y después los podés dejar guardados directamente en el `SKILL.md` de cada agente (en la sección **[COMPLETÁ ESTO]**) para no repetirlos cada vez.

## ¿No usás Claude Code?

Estas skills están pensadas para Claude Code, pero el contenido de cada `SKILL.md` es, en el fondo, un prompt muy detallado. Si usás Claude.ai (sin Claude Code), podés:

1. Abrir el `SKILL.md` del agente que quieras usar.
2. Copiar todo el contenido debajo de las líneas `---` del principio (eso es metadata, no hace falta pegarla).
3. Pegarlo al inicio de una conversación nueva en Claude.ai, y seguir la conversación desde ahí.

Vas a perder la activación automática (tenés que pegarlo manualmente cada vez), pero el agente funciona igual.
