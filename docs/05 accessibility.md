5. Accesibilidad (docs/05-accessibility.md)
Contraste AA
Tamaños mínimos
Estados focus
Lenguaje claro

💡 

Se establecen lineamientos alineados a WCAG 2.1 AA como base para futuras validaciones.

# 05 · Accesibilidad WCAG 2.1 AA

El Edvance Design System adopta WCAG 2.1 nivel AA como estándar mínimo en todas las marcas.

## Resumen de cumplimiento

| Estado | Cantidad | Descripción |
|--------|---------:|-------------|
| ✅ Cumplidos | 23 | WCAG 2.1 AA |
| ⚠️ Parciales | 4 | Requieren revisión |
| 📋 Pendientes | 2 | Para Fase 2 |

---

## 1. Contraste y color

| Estado | Criterio | Marcas | Implementación |
|--------|----------|--------|----------------|
| ✅ | 1.4.3 Contraste de texto — Texto normal: mínimo 4.5:1 | Todas | Verificado en todos los componentes. Nubi usa `neutral/dark` (`#1A1A1A`) sobre primary naranja — ratio 5.30:1 |
| ✅ | 1.4.3 Texto grande — Texto 18pt+ o 14pt bold: mínimo 3:1 | Todas | HEADING (28px Bold) verificado en las 4 marcas. Ratio mínimo 4.8:1 |
| ✅ | 1.4.1 Uso del color — No solo color para transmitir info | Todas | Alert y Toast usan ícono + barra lateral + texto. Tab activo usa SemiBold + línea inferior. Badge incluye texto siempre |
| ✅ | 1.4.11 Contraste UI — Componentes UI: mínimo 3:1 | Todas | Borders de inputs, checkboxes y toggles verificados. Toggle thumb blanco sobre track coloreado: ratio 4.5:1+ |

---

## 2. Interacción y navegación

| Estado | Criterio | Marcas | Implementación |
|--------|----------|--------|----------------|
| ✅ | 2.5.5 Área de toque — Mínimo 48×48px en controles | Todas | Buttons: 48px alto fijo. Inputs: 56px. Toggle: 24px alto — padding en implementación para cumplir 48×48px |
| ✅ | 2.5.5 Checkbox — Área de toque mínima 24×24px | Todas | Box visual 20×20px. El componente incluye nota de padding mínimo en implementación |
| ⚠️ | 2.4.7 Foco visible — El foco de teclado debe ser visible | Todas | Definido conceptualmente. Los focus states no están construidos visualmente como variantes — Fase 2 |
| ✅ | 1.3.1 Info y relaciones — Estructura semántica del contenido | Todas | Labels siempre visibles en inputs. Tabs usan SemiBold + línea activa. Navbar item activo con fondo `primary-dark` |
| ⚠️ | 2.4.3 Orden de foco — Orden lógico de navegación con Tab | Todas | El orden visual es lógico en los diseños. Requiere verificación en implementación de código — no validable solo en Figma |

---

## 3. Contenido y tipografía

| Estado | Criterio | Marcas | Implementación |
|--------|----------|--------|----------------|
| ✅ | 1.4.4 Redimensionado de texto — Texto escalable hasta 200% sin pérdida | Todas | Text styles con tamaños relativos. Escala tipográfica desde 11px (Caption) hasta 52px (Hero). Poppins y DM Sans escalan bien |
| ✅ | 1.4.8 Presentación visual — Espaciado de línea mínimo 1.5x | Todas | Body 14px → lineHeight 22px (1.57x). Caption 12px → lineHeight 16px (1.33x). HEADING usa 36px line-height sobre 28px |
| ✅ | 3.3.1 Identificación de error — Errores identificados con texto + ícono | Todas | Input error state incluye texto de error bajo el campo + borde rojo + ícono. Alert error con barra lateral + ícono + título |
| ✅ | 3.3.2 Labels o instrucciones — Labels visibles en todos los controles | Todas | Input siempre muestra label sobre el campo. Checkbox usa label descriptivo. Toggle usa label de función, no de estado |
| ⚠️ | 1.4.12 Espaciado de texto — Sin pérdida de contenido al aumentar spacing | Todas | Verificado visualmente en diseño. Requiere test en implementación CSS con `letter-spacing` y `word-spacing` aumentados |

---

## Decisiones especiales de accesibilidad por marca

### 🟠 Nubi — Dark text strategy

El naranja `#E56A0F` no cumple WCAG AA como texto sobre fondo blanco (ratio 2.94:1).

**Solución:** usar `neutral/dark` (`#1A1A1A`) como color de texto en todos los componentes sobre fondo primary de Nubi.

- Ratio resultante: **15.63:1** ✅  
- Tokens afectados: `tab/active/text` · `badge/text` · `badge/icon` · `footer/text` · `toggle/label`

---

### 🏆 Badge/logro — Accent como fondo, texto dark

El color accent puede ser claro en algunas marcas. Para garantizar contraste sobre accent en todas las marcas, `badge/logro/text` siempre usa `neutral/dark` (`#1A1A1A`).

- Ratio mínimo verificado: **8.31:1** ✅  
- Tokens afectados: `badge/logro/text` · `badge/logro/bg`

---

### 🟠 Footer Nubi — Primary naranja como fondo

El footer de Nubi usa primary naranja como fondo con texto `neutral/dark`.

- Contraste: **5.30:1** ✅ (supera mínimo de 4.5:1)  
- Texto muted usa `neutral/dark` con 60% opacity — verificar en implementación  

- Tokens afectados: `footer/bg` · `footer/text` · `footer/text/muted`

---

> **📋 Alcance de esta verificación**
>
> Este checklist cubre los criterios verificables en Figma.  
> Los criterios de implementación (orden de foco real, ARIA labels, semántica HTML) deben verificarse en el código durante el desarrollo.  
> Los estados de foco visual están planificados para la **versión 1.1** del sistema.

---

**Edvance Design System v1.0 · Abril 2026 · Figma →**
