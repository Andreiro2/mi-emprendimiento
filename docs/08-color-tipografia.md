# Color y tipografía — Joyas Kofran

> Guía: [Color y tipografía](../evaluacion/guias/fase-2-specs/05-color-y-tipografia.md)

## Paleta 

| Rol | Color | HEX | Uso |
|---|---|---|---|
| Principal | Azul noche | `#1F4E79` | Header, footer, botones principales (CTA), títulos destacados |
| Principal hover | Azul noche oscuro | `#183E60` | Estado hover y active de los botones principales |
| Secundario | Gris plata | `#C9CDD3` | Bordes, divisores, fondos de tarjetas y filtros, detalles que evocan la plata. No se usa para texto |
| Acento | Bronce dorado | `#8C5F22` | Enlaces, etiquetas ("Plata 925", "Garantía"), íconos, estados hover, precios destacados |
| Fondo | Marfil | `#FAF8F5` | Fondo general de landing, blog y tienda; las tarjetas de producto van sobre blanco `#FFFFFF` |
| Texto | Negro suave | `#1C1C1E` | Párrafos, descripciones de producto, texto de formularios |
| Texto secundario | Gris grafito | `#5C5C5C` | Fechas, categorías del blog, textos de ayuda bajo los campos |
| Éxito | Verde | `#2E7D4F` | Producto agregado al carrito, compra confirmada, formulario enviado |
| Error | Rojo | `#B3261E` | Campos inválidos, falta de stock, error de pago o de formulario |

## Contraste

| Combinación | Ratio | Resultado |
|---|---|---|
| Texto `#1C1C1E` sobre Fondo `#FAF8F5` | 16,05:1 | Pasa AAA |
| Blanco `#FFFFFF` sobre Principal `#1F4E79` (botones, header, footer) | 8,66:1 | Pasa AAA |
| Blanco `#FFFFFF` sobre Principal hover `#183E60` | 11,07:1 | Pasa AAA |
| Principal `#1F4E79` sobre Fondo `#FAF8F5` (títulos destacados) | 8,17:1 | Pasa AAA |
| Texto `#1C1C1E` sobre Secundario `#C9CDD3` | 10,66:1 | Pasa AAA |
| Texto secundario `#5C5C5C` sobre Fondo `#FAF8F5` | 6,31:1 | Pasa AA |
| Acento `#8C5F22` sobre Fondo `#FAF8F5` (enlaces, precios) | 5,25:1 | Pasa AA |
| Acento `#8C5F22` sobre Blanco `#FFFFFF` (precios en las tarjetas) | 5,56:1 | Pasa AA |
| Blanco `#FFFFFF` sobre Acento `#8C5F22` (etiquetas "Plata 925") | 5,56:1 | Pasa AA |
| Éxito `#2E7D4F` sobre Fondo `#FAF8F5` | 4,76:1 | Pasa AA |
| Error `#B3261E` sobre Fondo `#FAF8F5` | 6,17:1 | Pasa AA |

Ratios calculados con la fórmula de luminancia relativa de WCAG 2.1 (la misma del verificador de WebAIM).

## Tipografía

- **Títulos:** Cormorant Garamond (Google Fonts), serif elegante. Alternativa del sistema: Georgia, serif.
- **Textos:** Inter (Google Fonts), sans-serif de alta legibilidad. Alternativa del sistema: Arial, sans-serif.

| Elemento | Desktop | Mobile | Peso |
|---|---|---|---|
| h1 | 48 px | 32 px | 600 (Cormorant Garamond) |
| h2 | 36 px | 26 px | 600 (Cormorant Garamond) |
| h3 | 24 px | 20 px | 600 (Cormorant Garamond) |
| Párrafo | 16 px | 16 px | 400 (Inter), interlineado 1,6 |
| Botón | 16 px | 16 px | 600 (Inter), mayúsculas con espaciado de letras 0,5 px |

## Justificación

**Color.** Joyas Kofran vende plata ley 925 y su diferencial es la confiabilidad, la calidad con garantía y la buena atención. Por eso la paleta combina un azul noche, que transmite seriedad y confianza, con un gris plata que recuerda el material de las joyas. El fondo marfil le da calidez y un aire premium sin cansar la vista. El bronce dorado funciona como acento cálido para guiar la atención hacia enlaces, precios y etiquetas de garantía, y no compite con el azul de los botones principales. Los colores de éxito y error son estándar y se entienden de inmediato en el flujo de compra.

**Contraste.** Todas las combinaciones usadas para texto y botones superan el mínimo AA de WCAG (4,5:1). El acento se oscureció hasta `#8C5F22` porque un dorado más claro no alcanzaba ese mínimo sobre el fondo marfil. El gris plata solo se usa como elemento decorativo o de fondo, nunca como color de texto.

**Tipografía.** Cormorant Garamond, una serif elegante, aporta el carácter de joyería fina en los títulos. Inter se usa en descripciones, precios, formularios y botones por su legibilidad en pantallas pequeñas, donde compra la mayoría de los clientes. Dos familias son suficientes para mantener una identidad coherente y un sitio liviano, importante porque se publica solo con HTML y CSS en GitHub Pages. En mobile los títulos bajan de tamaño para evitar saltos de línea excesivos y el párrafo se mantiene en 16 px para que sea cómodo de leer.
