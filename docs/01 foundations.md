
1. Foundations (docs/01-foundations.md)

Incluye:

🎨 Color system (base + semantic)
🔤 Tipografía (escala)
📐 Espaciado (8pt system)
📏 Grid
🎞 Motion (principios, no hace falta animar todo)

Justificación:

Se definió una base neutral adaptable a múltiples marcas mediante theming.

# 01 · Paleta de colores por marca

Cada marca define su propia paleta de colores basada en los mismos roles semánticos.  
Los tokens globales (neutrales) son compartidos en todas las marcas.

## Edvance

| Token            | Nombre          | Hex     |
|------------------|-----------------|---------|
| primary          | primary         | #7C3AED |
| accent           | accent          | #7E4DD2 |
| primary-dark     | primary-dark    | #5622AF |
| primary-subtle   | p-subtle        | #F5F3FF |
| primary-light    | p-light         | #DDD8FE |

## Kira

| Token            | Nombre          | Hex     |
|------------------|-----------------|---------|
| primary          | primary         | #0943A1 |
| accent           | accent          | #2C6BC5 |
| primary-dark     | primary-dark    | #0A3580 |
| primary-subtle   | p-subtle        | #EEF4FF |
| primary-light    | p-light         | #BFDBFE |

## Blink

| Token            | Nombre          | Hex     |
|------------------|-----------------|---------|
| primary          | primary         | #07723A |
| accent           | accent          | #098142 |
| primary-dark     | primary-dark    | #00632F |
| primary-subtle   | p-subtle        | #EDFAF3 |
| primary-light    | p-light         | #BBEDD4 |

## Nubi

| Token            | Nombre          | Hex     |
|------------------|-----------------|---------|
| primary          | primary         | #E56A0F |
| accent           | accent          | #F5A050 |
| primary-dark     | primary-dark    | #CF6315 |
| background       | background      | #FFF0E6 |
| primary-light    | p-light         | #FECDAA |

## Neutrales globales (compartidos en todas las marcas)

| Token          | Hex     |
|----------------|---------|
| neutral/dark   | #1A1A1A |
| neutral/mid    | #888888 |
| neutral/light  | #F5F5F5 |

---

# 02 · Arquitectura de tokens

El sistema sigue una arquitectura de tres capas.  
Los componentes nunca consumen valores primitivos directamente.

**Global (raw) → Semantic → Componente**

| Valores       | Significado | Aplicación |
|---------------|------------|-----------|
| primitivos    | de uso     | final     |

---

## Color tokens (7)

| Token           | Descripción |
|-----------------|------------|
| primary         | Color principal de la marca |
| accent          | Color de acento / interactivo |
| background      | Fondo de página / superficie principal |
| primary-hover   | Versión oscura de primary para hover |
| text            | Color de texto principal |
| surface         | Fondo de componentes (cards, modales) |
| on-primary      | Texto sobre fondos primary · ⚠️ Nubi → usar neutral/dark |

---

## Button tokens (12)

| Token               | Descripción |
|--------------------|------------|
| primary/bg         | Fondo del botón Primary |
| primary/bg-hover   | Fondo en hover del Primary |
| primary/pressed    | Fondo en estado pressed |
| primary/label      | Texto del botón Primary |
| secondary/bg       | Fondo del botón Secondary |
| secondary/bg-hover | Fondo en hover del Secondary |
| secondary/label    | Texto del botón Secondary · ⚠️ Nubi → usar neutral/dark |
| ghost/label        | Texto del botón Ghost |
| ghost/bg-hover     | Fondo en hover del Ghost |
| disabled/bg        | Fondo del botón deshabilitado |
| disabled/label     | Texto del botón deshabilitado |
| disabled/border    | Borde del botón deshabilitado |

---

## Typography tokens (2)

| Token                | Resolución |
|----------------------|-----------|
| heading              | font/family/heading |
| body                 | font/family/body |

---

## Text styles (5)

| Estilo     | Especificación              |
|------------|---------------------------|
| HEADING    | 28px / 36px line-height   |
| HEADING 2  | 22px / 30px line-height   |
| Body       | 14px / 22px line-height   |
| Caption    | 12px / 16px line-height   |
| Button     | 14px / 20px line-height   |
# 03 · Tipografía

Cada marca tiene su propia combinación tipográfica.  
Todos comparten la misma escala de tamaños y pesos.

## Escala tipográfica completa

| Estilo     | Muestra | Especificación                          | Uso |
|------------|--------|------------------------------------------|-----|
| Display    | 52px · Bold | DM Sans Bold · 52/62 · tracking -1px | Hero sections, grandes titulares de landing |
| Heading 1  | 28px · Bold | Font heading · 28/36                | Títulos de página, sección principal |
| Heading 2  | 22px · Regular | Font heading · 22/30            | Títulos de cards y subsecciones |
| Body       | 14px · Regular | Font body · 14/22               | Texto de contenido general |
| Body SM    | 13px · Regular | Font body · 13/normal          | Subtítulos, texto de apoyo |
| Label      | 11px · Medium | Poppins · 11/16 · tracking 0.2px | Labels de componentes, badges |
| Caption    | 12px · Regular | Font body · 12/16             | Textos secundarios, meta-información |
| Button     | 14px · SemiBold | Font body · 14/20           | Texto de botones y CTAs |

---

## Pares tipográficos por marca

| Marca   | Heading            | Body             |
|---------|--------------------|------------------|
| Edvance | Montserrat Bold    | Poppins Regular  |
| Kira    | DM Sans Bold       | Poppins Regular  |
| Blink   | Nunito Bold        | Poppins Regular  |
| Nubi    | Nunito Bold        | Poppins Regular  |

---

## Identidad de marca

### Edvance
- **Segmento:** Design System · EdTech  
- **Tono de voz:** Innovador · Confiable · Escalable  
- **Colores:**  
  - primary: #7C3AED  
  - accent: #7E4DD2  
  - primary-dark: #5622AF  
  - p-subtle: #F5F3FF  
  - p-light: #DDD8FE  

### Kira
- **Segmento:** Plataforma profesional de cursos  
- **Tono de voz:** Profesional · Claro · Eficiente  
- **Colores:**  
  - primary: #0943A1  
  - accent: #2C6BC5  
  - primary-dark: #0A3580  
  - p-subtle: #EEF4FF  
  - p-light: #BFDBFE  

### Blink
- **Segmento:** Programas interactivos para adolescentes  
- **Tono de voz:** Dinámico · Motivador · Gamificado  
- **Colores:**  
  - primary: #07723A  
  - accent: #098142  
  - primary-dark: #00632F  
  - p-subtle: #EDFAF3  
  - p-light: #BBEDD4  

### Nubi
- **Segmento:** Programas de nivel inicial para niños  
- **Tono de voz:** Lúdico · Colorido · Accesible  
- **Colores:**  
  - primary: #E56A0F  
  - accent: #F5A050  
  - primary-dark: #CF6315  
  - background: #FFF0E6  
  - p-light: #FECDAA  

---

# 04 · Espaciado

Escala basada en múltiplos de 4px.  
Todos los valores de padding, margin y gap del sistema provienen de esta escala.

📐 **Regla del sistema:**  
Todos los valores de padding, gap y margin deben ser múltiplos de 4px.  
Nunca usar valores intermedios como 3px, 5px, 7px o 11px.  
Si necesitás un valor que no existe en la escala, usá el más cercano o solicitá la extensión de la escala.

---

## Escala base

| Token        | Valor | Alias   | Uso típico |
|--------------|------|--------|-----------|
| spacing/1    | 4px  | xs-xs  | Border radius pequeño, gaps mínimos |
| spacing/2    | 8px  | xs     | Gap entre ícono y label, padding chips |
| spacing/3    | 12px | xs-sm  | Padding interno de badges |
| spacing/4    | 16px | sm     | Padding horizontal de botones e inputs |
| spacing/5    | 20px | sm-md  | Gap entre elementos de formulario |
| spacing/6    | 24px | md     | Padding interno de cards y modales |
| spacing/8    | 32px | md-lg  | Gap entre componentes en una fila |
| spacing/10   | 40px | lg     | Padding de secciones compactas |
| spacing/12   | 48px | lg-xl  | Altura mínima de botones |
| spacing/16   | 64px | xl     | Padding horizontal de layout |
| spacing/20   | 80px | xl-2xl | Padding vertical de secciones hero |
| spacing/24   | 96px | 2xl    | Padding de secciones grandes |

---

## Tokens semánticos de uso

| Token                    | Valor | Dónde se usa |
|--------------------------|------|--------------|
| spacing/component/xs     | 4px  | Padding interno compacto — badges, chips, labels pequeños |
| spacing/component/sm     | 8px  | Gap entre elementos internos — ícono + label |
| spacing/component/md     | 16px | Padding estándar — botones, inputs, cards |
| spacing/component/lg     | 24px | Gap entre componentes — separación en grid |
| spacing/layout/section   | 60px | Padding vertical de sección |
| spacing/layout/page      | 80px | Padding horizontal de página |
| spacing/layout/gap       | 24px | Gap entre columnas del grid |
| spacing/layout/gap-lg    | 40px | Gap entre secciones |

---

# 05 · Sistema de grilla

El sistema define dos breakpoints principales: Desktop (1440px) y Mobile (390px).  
La grilla de 12 columnas en desktop y 4 en mobile garantiza consistencia y alineación.

---

## Especificaciones de breakpoints

| Breakpoint | Viewport | Columnas | Gutter | Margen | Uso |
|------------|----------|----------|--------|--------|-----|
| Desktop    | 1440px   | 12       | 24px   | 80px   | Layouts completos, dashboards, landing pages |
| Tablet     | 768px    | 8        | 20px   | 40px   | Adaptación intermedia |
| Mobile     | 390px    | 4        | 16px   | 24px   | Navegación, formularios, cards apiladas |

---

## Grilla Desktop — 1440px

|← 80px →| col | gut | col | gut | col | gut | col | gut | col | gut | col | gut | col | gut | col | gut | col | gut | col | gut | col | gut | col |← 80px →|
1 2 3 4 5 6 7 8 9 10 11 12


**Leyenda:**  
■ Columna (75px) · ░ Gutter (24px) · ▓ Margen (80px)

---

## Grilla Mobile — 390px

|←24px→| col 1 | gut | col 2 | gut | col 3 | gut | col 4 |←24px→|

**Leyenda:**  
■ Columna (73px) · ░ Gutter (16px) · ▓ Margen (24px)

---

## Reglas de uso

| #  | Regla                         | Descripción |
|----|-------------------------------|-------------|
| 01 | Nunca romper los márgenes     | El contenido siempre queda dentro de los márgenes |
| 02 | Columnas completas siempre    | No usar medias columnas ni valores intermedios |
| 03 | El gutter no es espacio extra | El gutter solo separa columnas |
| 04 | Mobile first                 | Diseñar en 390px primero, luego escalar |
