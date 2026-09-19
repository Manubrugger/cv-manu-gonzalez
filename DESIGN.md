---
colors:
  primary: "#0E1033"          # Azul oscuro
  secondary: "#D5DE24"        # Verde lima
  accent: "#ED2B5F"           # Rosa
  neutral: "#D6D6D6"          # Gris claro
  white: "#FFFFFF"            # Blanco
typography:
  fontFamily: "AsapSharp"
  fontFiles:
    - "assets/fonts/AsapSharp-VariableFont.woff2"
  scale:
    displayLarge: "clamp(72px, 8vw, 120px)"  # Títulos muy grandes
    displayMedium: "clamp(56px, 6vw, 72px)"   # H1
    displaySmall: "clamp(40px, 5vw, 56px)"    # H2
    headlineMedium: "clamp(24px, 3vw, 32px)"  # H3
    bodyLarge: "clamp(18px, 2vw, 20px)"       # Cuerpo de texto
    bodySmall: "clamp(14px, 1.5vw, 16px)"     # Texto pequeño
  lineHeight:
    tight: 1.1
    normal: 1.5
    relaxed: 1.7
  fontWeight:
    regular: 400
    medium: 500
    bold: 700
spacing:
  base: 8
  scale:
    - 8
    - 16
    - 24
    - 32
    - 48
    - 64
    - 96
    - 128
  sectionGap: 96
  maxContentWidth: 1400
  gridColumns: 12
rounded:
  none: 0
  sm: 8
  md: 16
  lg: 24
  pill: 9999
components:
  button:
    primary:
      bg: "{colors.primary}"
      color: "{colors.white}"
      hover:
        bg: "{colors.secondary}"
        color: "{colors.primary}"
        transform: "translateY(-2px) scale(1.02)"
    secondary:
      bg: "transparent"
      border: "2px solid {colors.primary}"
      color: "{colors.primary}"
      hover:
        bg: "{colors.secondary}"
        borderColor: "{colors.secondary}"
        color: "{colors.primary}"
    tertiary:
      bg: "{colors.secondary}"
      color: "{colors.primary}"
      hover:
        bg: "{colors.primary}"
        color: "{colors.white}"
  card:
    bg:
      - "{colors.white}"
      - "{colors.neutral}"
      - "{colors.primary}"
    hover:
      transform: "translateY(-4px)"
      boxShadow: "0 8px 24px rgba(14, 16, 51, 0.12)"
    borderRadius: "{rounded.md}"
  nav:
    fontFamily: "{typography.fontFamily}"
    color: "{colors.primary}"
    hoverColor: ["{colors.accent}", "{colors.secondary}"]
    transition: "color 150ms ease"
  tag:
    borderRadius: "{rounded.pill}"
    bgOptions: ["{colors.secondary}", "{colors.accent}", "{colors.neutral}", "{colors.primary}"]
    padding: "4px 12px"
    fontSize: "{typography.scale.bodySmall}"
  scrollText:
    text: "SOBRE MÍ · SOBRE MÍ · SOBRE MÍ · SOBRE MÍ ·"
    fontFamily: "{typography.fontFamily}"
    fontSize: "clamp(72px, 12vw, 120px)"
    bg: "{colors.primary}"
    color: "{colors.secondary}"
    animationDuration: "30s"
    animationTiming: "linear"
---

# Overview

Este sistema de diseño define la identidad visual de mi marca personal: una mezcla entre currículum, portafolio y página creativa. La personalidad busca ser **amigable, confiable y disruptiva** a la vez. La confianza se transmite mediante el azul oscuro, una estructura clara y textos legibles; la disrupción aparece en los acentos verde lima y rosa, títulos de gran tamaño y animaciones sutiles. El objetivo es una experiencia fácil de recorrer, con momentos visuales que sorprendan sin dificultar la lectura.

---

# Colors

La paleta se compone de **cuatro colores principales** más blanco como fondo de apoyo.

| Token | Hex | Rol | Uso principal |
|-------|-----|-----|---------------|
| `colors.primary` | `#0E1033` | **Azul oscuro** | Color de confianza y profesionalidad. Fondos oscuros, títulos, botones primarios, **cuerpo de texto sobre fondos claros**. |
| `colors.secondary` | `#D5DE24` | **Verde lima** | Color disruptivo de acento. Botones, palabras clave, detalles gráficos, etiquetas, algunos fondos. **Texto sobre él: `colors.primary`**. Usar con moderación. |
| `colors.accent` | `#ED2B5F` | **Rosa** | Segundo color disruptivo. **Solo para elementos decorativos, bloques de color, títulos grandes, números grandes, acentos, íconos y hover**. **NO usar para cuerpo de texto, texto pequeño ni textos largos sobre fondo blanco o azul oscuro** (no cumple WCAG AA 4.5:1). |
| `colors.neutral` | `#D6D6D6` | **Gris claro** | Calma visual. Fondos secundarios, divisiones, **cuerpo de texto sobre fondos oscuros (`colors.primary`)**. **No usar para párrafos sobre blanco** (contraste insuficiente). |
| `colors.white` | `#FFFFFF` | **Blanco** | Fondo de tarjetas, secciones claras y texto sobre fondos oscuros. |

**Reglas de contraste obligatorias:**
- **Cuerpo de texto largo** → `colors.primary` (`#0E1033`) sobre fondos claros (`colors.white`, `colors.neutral`); `colors.neutral` (`#D6D6D6`) sobre fondo `colors.primary` (`#0E1033`).
- **Títulos grandes** (`displayLarge`–`displaySmall`) → pueden usar cualquier color de la paleta **si cumplen contraste WCAG AA** (tamaño ≥ 24px o ≥ 19px bold permite 3:1).
- Sobre `colors.secondary` (verde lima) → texto en `colors.primary` (`#0E1033`).
- **Rosa (`colors.accent`)** → **prohibido para texto de lectura** (cuerpo, small, párrafos). Solo en elementos gráficos de gran tamaño donde la legibilidad no se comprometa.

---

# Typography

**Fuente única:** **AsapSharp** (variable font, `assets/fonts/AsapSharp-VariableFont.woff2`). Toda la página usa esta tipografía variando tamaño y peso.

## Escala tipográfica (clamp para fluidez)

| Token | Clamp | Uso |
|-------|-------|-----|
| `typography.scale.displayLarge` | `clamp(72px, 8vw, 120px)` | Títulos hero / "SOBRE MÍ" scroll |
| `typography.scale.displayMedium` | `clamp(56px, 6vw, 72px)` | H1 |
| `typography.scale.displaySmall` | `clamp(40px, 5vw, 56px)` | H2 |
| `typography.scale.headlineMedium` | `clamp(24px, 3vw, 32px)` | H3 |
| `typography.scale.bodyLarge` | `clamp(18px, 2vw, 20px)` | Cuerpo principal |
| `typography.scale.bodySmall` | `clamp(14px, 1.5vw, 16px)` | Texto pequeño, etiquetas |

## Interlineado
- `typography.lineHeight.tight` (1.1) → títulos grandes
- `typography.lineHeight.normal` (1.5) → cuerpo de texto
- `typography.lineHeight.relaxed` (1.7) → párrafos extensos

## Pesos
- `typography.fontWeight.regular` (400) → cuerpo
- `typography.fontWeight.medium` (500) → énfasis
- `typography.fontWeight.bold` (700) → títulos

---

# Layout

- **Espaciado base:** 8px (`spacing.base`). Escala: 8, 16, 24, 32, 48, 64, 96, 128px (`spacing.scale`).
- **Separación entre secciones principales:** `spacing.sectionGap` (96px).
- **Ancho máximo de contenido:** `spacing.maxContentWidth` (1400px) en escritorio.
- **Retícula:** 12 columnas (`spacing.gridColumns`) en desktop.
- **Principio:** amplio espacio negativo ("aire"), no todo rígido. Algunos títulos/elementos **pueden romper la retícula** intencionadamente para interés visual.
- **Párrafos:** ancho limitado para legibilidad (no full-width).
- **Combinación:** secciones limpias + secciones con protagonismo de color/tipografía.

### Breakpoints (referencia)
| Dispositivo | Columnas | Márgenes laterales |
|-------------|----------|-------------------|
| Desktop | 12 | Auto (centrado ≤1400px) |
| Tablet | 1-2 | ~32px |
| Mobile | 1 | 16-24px (`spacing.scale[1]`–`spacing.scale[2]`) |

---

# Elevation & Depth

**Diseño predominantemente plano.** La profundidad se logra con **color, espacio, líneas y escala**, no con sombras pesadas.

- **Tarjetas:** planas por defecto. `boxShadow` ligero solo en `:hover` (`components.card.hover.boxShadow`).
- **Sombras:** nunca fuertes; `rgba(14, 16, 51, 0.12)` máx.
- **Interacciones:** cambios de color, micro-movimientos (`translateY`), escalado sutil, transiciones 150–250ms ease.

---

# Shapes

- **Contenedores:** esquinas rectas o `rounded.sm` (8px) → `components.card.borderRadius`.
- **Elementos destacados:** `rounded.md` (16px) o `rounded.lg` (24px).
- **Botones:** más redondeados para resaltar (`rounded.md` o `rounded.lg`).
- **Etiquetas / botones pequeños:** `rounded.pill` (9999px) → `components.tag.borderRadius`.
- **Sin formas decorativas innecesarias**; la estructura vive de tipografía, color, bloques y movimiento.

---

# Components

## Navegación (`components.nav`)
- Texto: `typography.fontFamily` (AsapSharp).
- Color reposo: `colors.primary` (sobre fondo claro).
- Hover: `colors.accent` o `colors.secondary` (transición 150ms ease).
- Mobile: menú hamburguesa.

## Botones
| Variante | Reposo | Hover |
|----------|--------|-------|
| **Primario** (`components.button.primary`) | `bg: colors.primary`, `color: colors.white` | `bg: colors.secondary`, `color: colors.primary`, `transform: translateY(-2px) scale(1.02)` |
| **Secundario** (`components.button.secondary`) | Transparente, `border: 2px solid colors.primary`, `color: colors.primary` | `bg: colors.secondary`, `borderColor: colors.secondary`, `color: colors.primary` |
| **Terciario** (`components.button.tertiary`) | `bg: colors.secondary`, `color: colors.primary` | `bg: colors.primary`, `color: colors.white` |

**Reglas de contraste en botones:**
- Priorizar combinaciones seguras: fondo `colors.primary` + texto `colors.white` (18.4:1), fondo `colors.secondary` + texto `colors.primary` (12.5:1).
- **Evitar botón rosa (`colors.accent`) con texto pequeño** si no cumple WCAG AA. El hover rosa en secundario/terciario usa fondo rosa solo en tamaños grandes (≥ 24px) o con texto blanco en botones grandes; en botones pequeños/texto pequeño, el hover secundario/terciario usa verde o azul.

## Tarjetas (`components.card`)
- Fondos permitidos: `colors.white`, `colors.neutral`, `colors.primary`.
- Usar `colors.white` para tarjetas en secciones claras; `colors.neutral` para secciones alternadas; `colors.primary` para secciones oscuras.
- No todas las secciones usan tarjetas; alternar con líneas/espacio.
- Hover: `translateY(-4px)` + sombra ligera.
- Border radius: `rounded.md` (16px).

## Etiquetas / Tags (`components.tag`)
- Forma píldora (`rounded.pill`).
- Fondos: `colors.secondary`, `colors.accent`, `colors.neutral`, `colors.primary` según contexto.
- **Si el fondo es `colors.accent` (rosa), usar solo en etiquetas grandes/íconos, no en texto pequeño de lectura.**
- Padding: 4px 12px. Tamaño: `bodySmall`.

## Texto scroll "SOBRE MÍ" (`components.scrollText`)
- Contenido: `"SOBRE MÍ · SOBRE MÍ · SOBRE MÍ · SOBRE MÍ ·"`
- Full-width, horizontal scroll infinito (CSS animation).
- `fontSize`: `clamp(72px, 12vw, 120px)`, `fontFamily`: AsapSharp.
- Ejemplo: `bg: colors.primary`, `color: colors.secondary`.
- Duración: ~30s, `linear`, fluida.
- Mobile: tamaño reducido, velocidad menor.

## Animaciones globales
- **Entrada (scroll):** `translateY(20px) → 0`, `opacity: 0 → 1`, 400–600ms ease-out.
- **Hover botones/tarjetas:** color + `translateY(-2px…-4px)` + scale sutil, 150–200ms ease.
- **Reducir en mobile** (`prefers-reduced-motion` y ancho < 640px) para rendimiento.

---

# Do's and Don'ts

## ✅ Do's
- Usar `colors.primary` (`#0E1033`) para **cuerpos de texto** sobre fondos claros (`colors.white`, `colors.neutral`).
- Usar `colors.neutral` (`#D6D6D6`) para **cuerpos de texto** solo sobre fondo `colors.primary` (`#0E1033`).
- Usar `colors.secondary` (verde) y `colors.accent` (rosa) **solo para acentos gráficos**: botones, palabras clave, detalles, bloques de color, números grandes, títulos grandes, íconos.
- Usar **AsapSharp en toda la página** (pesos/tamaños según jerarquía).
- Usar **títulos grandes** (`displayLarge`–`displaySmall`) como elemento gráfico.
- Dejar **aire generoso** (`spacing.sectionGap`, escala 8px).
- Animaciones **suaves, breves, con propósito** (guían, no distraen).
- Permitir que **algunos títulos rompan la retícula** intencionadamente.
- Mantener **contraste WCAG AA** en todos los pares texto/fondo de lectura.
- Usar `colors.white` (`#FFFFFF`) como fondo de **tarjetas y secciones claras**.
- Diseñar **claro, escaneable, fácil de recorrer**.

## ❌ Don'ts
- ❌ Usar `colors.neutral` (gris claro) para **párrafos sobre fondo blanco** (contraste insuficiente).
- ❌ Usar verde (`secondary`) o rosa (`accent`) para **textos de lectura** (cuerpo, small, párrafos).
- ❌ Usar **rosa (`colors.accent`)** para **cuerpo de texto, texto pequeño o textos largos** sobre fondo blanco o azul oscuro (no alcanza 4.5:1).
- ❌ Usar **todos los colores a la vez** sin necesidad jerárquica.
- ❌ Abusar de **sombras** (diseño plano preferido).
- ❌ **Llenar todos los espacios** (el aire es parte del diseño).
- ❌ **Animaciones excesivas** o que dificulten lectura.
- ❌ Introducir **otras tipografías** salvo necesidad técnica justificada.
- ❌ Hacer el **cuerpo de texto < 18px** (mínimo `bodyLarge`).
- ❌ Poner texto de lectura sobre fondos sin **contraste válido** (≥ 4.5:1).
- ❌ Que la página parezca un **currículum tradicional y aburrido**.

---

> **Notas de revisión**  
> - `spacing.sectionGap` (96px) y `maxContentWidth` (1400px) son valores iniciales; ajustar tras pruebas visuales.  
> - `components.scrollText.animationDuration` (30s) es estimado; probar en distintos anchos.  
> - Pesos de variable font AsapSharp: confirmar que 400/500/700 existen en el archivo `.woff2`.  
> - Breakpoints exactos (px) para tablet/mobile: definir en tokens CSS si se requiere mayor precisión.