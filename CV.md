# Mi Landing de CV

Arquitectura de información, diseño y contenido.
El aspecto visual sigue las reglas de `DESIGN.md` (única fuente de verdad del diseño).

---

## 1. Estructura general y navegación

- Landing de **una sola página** (one-page).
- **Menú fijo superior** (`<header>` sticky), visible durante el scroll.
- Enlaces a secciones: **Sobre mí · Educación · Proyectos · Habilidades · Contacto**.
- Navegación sencilla y fácil de entender.
- En celular: **menú hamburguesa**.
- Responsive: computadora, tableta y celular.

**Secciones e IDs:**

| Orden | Sección    | ID           | Nav |
|-------|------------|--------------|-----|
| 1     | Inicio     | `#inicio`    | —   |
| 2     | Sobre mí   | `#sobre-mi`  | ✓   |
| 3     | Educación  | `#educacion` | ✓   |
| 4     | Proyectos  | `#proyectos` | ✓   |
| 5     | Habilidades| `#habilidades`| ✓  |
| 6     | Contacto   | `#contacto`  | ✓   |

---

## 2. Inicio (Hero) — `#inicio`

- Composición **muy limpia**, con bastante espacio libre.
- Nombre: **Manú González** (título principal, `displayLarge`/`displayMedium`).
- Subtítulo: **Diseño Gráfico**.
- **Foto** como elemento principal de la composición, al lado del texto.
- Sin exceso de texto ni botones: presentación rápida y visual.
- Desktop: texto y foto **lado a lado**. Celular: **uno arriba del otro**.

> REVISAR: falta el archivo de la foto en `assets/`. Se usará un placeholder accesible hasta recibirla.

---

## 3. Sobre mí — `#sobre-mi`

- **Transición previa**: marquesina `components.scrollText` con el texto
  `SOBRE MÍ · SOBRE MÍ · SOBRE MÍ · SOBRE MÍ ·`, movimiento horizontal ligado al scroll.
- Contenido: **una sola descripción breve** (protagonista, mucho aire):

> “Creo en el poder del diseño gráfico como una herramienta para generar soluciones creativas, explorar nuevos límites y aportar nuevas perspectivas a cada proyecto. Mi objetivo es transformar ideas en imágenes memorables y funcionales, buscando siempre un equilibrio entre estética y significado.”

- Sección sencilla, sin elementos extra.

---

## 4. Educación — `#educacion`

Formación en tarjetas o bloques separados (programa, institución, fechas). Orden:

1. **Diseño Gráfico Digital** — Universidad La Salle · `2023–2027`
   Actualmente curso el séptimo semestre de ocho.
2. **Graphic Design Course** — EduMac Digital Arts School · `2023`

Sin información extra.

---

## 5. Proyectos — `#proyectos`

- Una de las **secciones más visuales**. Formato **galería continua con scroll horizontal** (no cuadrícula).
- Cada proyecto: **imagen/mockup protagonista** + nombre + descripción muy corta.
- Orden:

| # | Proyecto | Tipo | Descripción |
|---|----------|------|-------------|
| 1 | Dr Pepper | Diseño de empaque | Proyecto de diseño de empaque para Dr Pepper. |
| 2 | Feria del Libro de Aguascalientes | Branding | Proyecto de creación de identidad visual para la Feria del Libro de Aguascalientes. |
| 3 | Qantas | Rediseño de identidad visual | Proyecto de rediseño de la identidad visual de la aerolínea Qantas. |
| 4 | Antica | Diseño de etiquetas | Diseño de etiquetas para una línea de salsas para pasta llamada Antica. |
| 5 | Olab | Rediseño | Proyecto de rediseño para el laboratorio Olab. |

- Desktop: el scroll vertical de la sección **avanza horizontalmente** entre proyectos; cada proyecto ocupa suficiente espacio para apreciar la imagen.
- Hover: interacción sencilla (la imagen crece un poco, se mueve ligeramente o aparece info adicional). Animaciones suaves.
- Celular: scroll horizontal táctil adaptado a pantalla.

> REVISAR: faltan las 5 imágenes/mockups en `assets/`. Se usarán placeholders accesibles con el nombre del proyecto hasta recibirlas.

---

## 6. Habilidades — `#habilidades`

Dos bloques: en computadora **dos columnas**, en celular **uno debajo del otro**.

### Programas

Escala visual de **5 círculos** por programa (rellenos = nivel, vacíos = restante). No barras de progreso. Círculos en colores del sistema.

| Programa | Nivel | Visual |
|----------|-------|--------|
| Adobe Illustrator | 5/5 | ● ● ● ● ● |
| Adobe Photoshop | 4/5 | ● ● ● ● ○ |
| Adobe InDesign | 4/5 | ● ● ● ● ○ |
| Figma | 3/5 | ● ● ● ○ ○ |
| Adobe After Effects | 3/5 | ● ● ● ○ ○ |

> Accesibilidad: cada escala lleva texto alternativo (`aria-label`, p. ej. “Adobe Photoshop: 4 de 5”).

### Soft Skills

Lista principalmente **tipográfica y sencilla**:

- Aprendizaje continuo
- Trabajo en equipo
- Atención al detalle
- Pensamiento innovador
- Capacidad para recibir y aplicar feedback
- Adaptabilidad

---

## 7. Contacto — `#contacto`

Cierre sencillo, solo dos vías como enlaces/botones del sistema de diseño:

- **Correo**: `manuglezb@yahoo.com` → `mailto:`, abre la app de correo.
- **LinkedIn**: `https://www.linkedin.com/in/man%C3%BA-gonz%C3%A1lez-30b43a216/` → abre el perfil (nueva pestaña, `rel="noopener"`).

Sin información extra.

---

## Notas de construcción

- Diseño (colores, tipografía, espaciado, radios, componentes, animaciones) derivado **únicamente** de los tokens de `DESIGN.md`.
- HTML semántico (`header`, `main`, `section`, `footer`, headings en orden), mobile-first, vanilla.
- Accesible: contraste AA (solo pares de texto seguros), foco visible, `prefers-reduced-motion`, etiquetas ARIA donde aplique.
- Assets pendientes del autor: **foto de perfil** + **5 imágenes de proyectos** (ver REVISAR arriba).
