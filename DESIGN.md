---
version: alpha
name: Joyas Kofran
description: "Design system de Joyas Kofran: joyería de plata ley 925 que se ve fina y se siente segura de comprar desde el celular."
colors:
  primary: "#1F4E79"
  primary-hover: "#183E60"
  on-primary: "#FFFFFF"
  secondary: "#C9CDD3"
  on-secondary: "#1C1C1E"
  tertiary: "#8C5F22"
  tertiary-hover: "#6F4A1A"
  on-tertiary: "#FFFFFF"
  neutral: "#FAF8F5"
  surface: "#FFFFFF"
  on-surface: "#1C1C1E"
  on-surface-variant: "#5C5C5C"
  disabled: "#D6D6D6"
  on-disabled: "#4A4A4A"
  success: "#2E7D4F"
  error: "#B3261E"
typography:
  headline-display:
    fontFamily: Cormorant Garamond
    fontSize: 48px
    fontWeight: 600
    lineHeight: 1.1
  headline-lg:
    fontFamily: Cormorant Garamond
    fontSize: 36px
    fontWeight: 600
    lineHeight: 1.2
  headline-md:
    fontFamily: Cormorant Garamond
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.25
  title-sm:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1.4
  price-md:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: 600
    lineHeight: 1.3
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  label-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.5px
  label-sm:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.5px
rounded:
  sm: 4px
  md: 8px
  full: 9999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  2xl: 48px
  3xl: 64px
components:
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
  text-secondary:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface-variant}"
    typography: "{typography.body-sm}"
  navbar:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    height: 72px
    padding: 0 24px
  footer:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.body-sm}"
    padding: 48px 24px
  trust-bar:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    typography: "{typography.body-sm}"
    padding: 8px 16px
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
    height: 48px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
  button-primary-active:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
  button-primary-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
    height: 48px
  button-secondary-hover:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.primary-hover}"
  button-secondary-active:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.primary-hover}"
  button-secondary-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  button-whatsapp:
    backgroundColor: "{colors.success}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
    height: 48px
  link:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.tertiary}"
    typography: "{typography.body-md}"
  link-hover:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.tertiary-hover}"
  tag-925:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-tertiary}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.full}"
    padding: 4px 10px
  chip-filter:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.full}"
    padding: 8px 16px
    height: 44px
  chip-filter-hover:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
  chip-filter-active:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
  chip-filter-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  search-bar:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.full}"
    padding: 12px 20px
    height: 48px
  input-field:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 12px 14px
    height: 48px
  input-field-error:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.error}"
  input-field-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  size-selector:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.md}"
    size: 48px
  size-selector-hover:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.primary}"
  size-selector-active:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
  size-selector-disabled:
    backgroundColor: "{colors.disabled}"
    textColor: "{colors.on-disabled}"
  card-product:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.title-sm}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  card-product-hover:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
  card-product-disabled:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface-variant}"
  price:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.tertiary}"
    typography: "{typography.price-md}"
  card-category:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    typography: "{typography.headline-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  card-article:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.title-sm}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  card-article-hover:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
  card-review:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.lg}"
  benefit-item:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-sm}"
    padding: "{spacing.md}"
  lead-form:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.xl}"
  cart-summary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: "{spacing.lg}"
  message-success:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.success}"
    typography: "{typography.body-sm}"
  message-error:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.error}"
    typography: "{typography.body-sm}"
---

# Joyas Kofran — Design system

## Overview

Joyas Kofran vende joyas de plata ley 925 en Chile por canales digitales. Su promesa es confiabilidad: piezas de calidad, con garantía y con atención cercana para elegir bien, ya sea para darse un gusto o para regalar.

La usuaria principal es **Camila Rojas (28)**, analista de RR. HH. en Viña del Mar. Llega desde Instagram o Google, casi siempre desde el celular y de noche, con un presupuesto de $25.000 a $60.000. Desconfía de las joyas que se oxidan, de las fotos editadas y de los perfiles sin respaldo, y antes de pagar necesita ver la medida, la prueba de que es plata 925, el costo del despacho y un WhatsApp que responda.

La interfaz debe transmitir las palabras clave del moodboard: **elegancia, calidad, brillo, confianza y sofisticación**, pero con un tono **cercano y claro**, no de lujo inalcanzable. Es una joyería fina de barrio digital, no una casa de alta joyería: se habla de plata 925, precios en pesos chilenos y atención por WhatsApp; nunca de diamantes, oro u "inversión".

## Colors

- **Primary (#1F4E79), azul noche:** navbar, footer, botón principal, chip y talla seleccionados, formulario de leads y títulos destacados. Transmite seriedad y confianza. No se usa para textos largos ni como fondo de secciones completas fuera del header, footer y bloque de leads.
- **Primary hover (#183E60):** hover y active del botón principal.
- **Secondary (#C9CDD3), gris plata:** bordes de tarjetas e inputs, divisores, barra de confianza y hover de chips. Evoca el metal. **Nunca** se usa como color de texto.
- **Tertiary (#8C5F22), bronce dorado:** acento cálido para precios, enlaces y la etiqueta `tag-925`. Máximo un elemento de acento por tarjeta. No se usa en botones principales para no competir con el azul.
- **Neutral (#FAF8F5), marfil:** fondo general de todas las páginas.
- **Surface (#FFFFFF):** fondo de tarjetas, inputs, carrito y fotos de producto, para que la plata se vea con su color real.
- **On-surface (#1C1C1E):** texto principal. **On-surface-variant (#5C5C5C):** fechas, categorías, textos de ayuda.
- **Success (#2E7D4F):** confirmaciones y botón de WhatsApp. **Error (#B3261E):** campos inválidos y falta de stock.
- **Disabled (#D6D6D6 con texto #4A4A4A):** tallas agotadas y botones deshabilitados.

Todas las combinaciones de texto cumplen WCAG AA (mínimo 4,5:1); el detalle está en `docs/08-color-tipografia.md`.

## Typography

- **Títulos (h1, h2, h3):** Cormorant Garamond 600. Da el carácter de joyería fina.
- **Textos, precios, botones y formularios:** Inter. Se lee bien en pantallas pequeñas.
- Solo estas dos familias, cargadas desde Google Fonts.

| Token | Uso | Desktop | Mobile |
|---|---|---|---|
| `headline-display` | h1 | 48px | 32px |
| `headline-lg` | h2 | 36px | 26px |
| `headline-md` | h3 y nombre de categoría | 24px | 20px |
| `title-sm` | Nombre de producto y título de artículo en tarjetas | 16px | 16px |
| `price-md` | Precios | 18px | 18px |
| `body-md` | Párrafos (interlineado 1,6) | 16px | 16px |
| `body-sm` | Textos de ayuda, fechas, barra de confianza | 14px | 14px |
| `label-md` | Botones (mayúsculas, espaciado 0,5px) | 16px | 16px |
| `label-sm` | Etiquetas `tag-925` | 13px | 13px |

El texto de párrafo nunca baja de 16px en mobile.

## Layout

- **Contenedor:** ancho máximo 1200px, centrado. Márgenes laterales de 16px en mobile, 24px en tablet y 32px en desktop.
- **Espaciado:** escala de 4, 8, 16, 24, 32, 48 y 64px. Entre secciones: 48px en mobile y 64px en desktop.
- **Breakpoints y comportamiento:**

| Elemento | Mobile (hasta 767px) | Tablet (768–1023px) | Desktop (desde 1024px) |
|---|---|---|---|
| Navbar | Logo, ícono de búsqueda, carrito y menú hamburguesa | Igual que mobile | Logo, Tienda, Blog, Contacto, buscador y carrito en una línea |
| Grilla de productos | 1 columna | 2 columnas | 3 columnas (4 en la landing) |
| Filtros de la tienda | Chips con scroll horizontal + botón "Filtrar" que abre un panel | Chips + panel desplegable | Columna lateral izquierda de 240px |
| Tarjetas de artículos | 1 columna | 2 columnas | 3 columnas |
| Ficha de producto | Galería arriba, información debajo | Galería arriba, información debajo | Galería a la izquierda (60 %) e información a la derecha (40 %) |
| Carrito | Lista arriba y `cart-summary` debajo | Igual que mobile | Lista a la izquierda y `cart-summary` fijo a la derecha |
| Footer | Columnas apiladas | 2 columnas | 4 columnas |

- En mobile el botón "Agregar al carrito" de la ficha queda fijo en la parte inferior de la pantalla.
- El `button-whatsapp` flotante va abajo a la derecha en todas las pantallas, a 16px de los bordes, y no tapa el botón fijo de la ficha.
- Todo elemento táctil mide al menos 44×44px. No hay scroll horizontal salvo en la fila de chips.
- Las fotos de producto son cuadradas (1:1); las de artículos, 16:9.

## Elevation & Depth

- La jerarquía se marca con **bordes y capas de color**, no con sombras fuertes: las tarjetas blancas (`surface`) se separan del fondo marfil con un borde de 1px `#C9CDD3`.
- Única sombra permitida: `0 4px 12px rgba(31, 78, 121, 0.12)` en el hover de `card-product` y `card-article`, y en el `cart-summary` fijo de desktop.
- El navbar queda fijo arriba al hacer scroll, con la misma sombra.
- El panel de filtros en mobile y el menú hamburguesa se abren sobre una capa `rgba(28, 28, 30, 0.5)`.

## Shapes

- **Botones, chips, buscador y `tag-925`:** completamente redondeados (`rounded.full`).
- **Tarjetas, inputs, selector de talla, carrito y formulario de leads:** 8px (`rounded.md`).
- **Fotos dentro de tarjetas:** 4px (`rounded.sm`) en las esquinas superiores.
- Los íconos son de línea, de 24px y 1,5px de trazo.

## Components

### Navbar (`navbar`)

Fondo azul `primary` en todas las pantallas. Logo "Joyas Kofran" a la izquierda; enlaces **Tienda, Blog y Contacto**; buscador e ícono de carrito con la cantidad de piezas. Siempre esos tres enlaces, en ese orden; no se agregan "Colecciones", "Atelier" ni "Sobre nosotros". La página actual se marca con subrayado de 2px.

### Barra de confianza (`trust-bar`)

Franja sobre el navbar con tres mensajes: "Plata ley 925 certificada", "Joyas con garantía" y "Despacho a todo Chile". En mobile rota un mensaje a la vez.

### Botones (`button-primary`, `button-secondary`, `button-whatsapp`)

- Un solo `button-primary` por sección; las acciones secundarias usan `button-secondary` (fondo blanco, borde de 1px y texto azul).
- Texto en verbos concretos: "Ver colección", "Agregar al carrito", "Ir a pagar". Nunca "Discover now" ni textos en inglés.
- `button-whatsapp` siempre dice "Consultar por WhatsApp" y lleva el ícono de WhatsApp. Abre un mensaje con el nombre de la pieza ya escrito.
- Estados: hover (color más oscuro), active (igual al hover), foco (contorno de 2px `#8C5F22` separado 2px) y disabled (gris, sin cursor de mano).

### Etiqueta (`tag-925`)

Pastilla bronce con texto blanco: "Plata 925", "Nuevo" o "Para regalar". Máximo una etiqueta por tarjeta, en la esquina superior izquierda de la foto.

### Buscador (`search-bar`) y filtros (`chip-filter`)

- Buscador con placeholder "Busca anillos, cadenas, aros…".
- Chips de categoría: Todas, Anillos, Cadenas y collares, Aros, Pulseras, Dijes. Uno solo activo a la vez.
- Filtros: Precio (Hasta $20.000, $20.000–$40.000, $40.000–$60.000, Más de $60.000), Ocasión (Para mí, Para regalar, Ocasiones especiales) y Medida.
- Estados: normal (borde gris plata), hover (fondo gris plata), active (fondo azul, texto blanco), disabled (gris, cuando no hay productos con ese filtro).

### Product card (`card-product`)

Foto cuadrada sobre fondo blanco, `tag-925`, nombre, tipo de pieza en `text-secondary`, precio en `price` y `button-secondary` "Ver producto".

- El precio siempre es visible y está en pesos chilenos con punto de miles: **$29.990**. Nunca USD ni decimales.
- El nombre ocupa máximo 2 líneas; si es más largo, termina en "…".
- La foto es de la pieza real; no renders ni fondos negros.
- Hover: sombra suave y la foto se agranda al 103 %.
- Agotado (`card-product-disabled`): foto en escala de grises, etiqueta "Agotado" y botón deshabilitado.

### Category card (`card-category`)

Foto de la pieza y nombre de la categoría en `headline-md`. Toda la tarjeta es un enlace a la tienda filtrada.

### Ficha de producto

Galería (foto principal + 3 miniaturas, al menos una en uso real), nombre (h1), `tag-925`, precio, selector de talla o largo, enlace "Ver guía de tallas", tabla de medidas (largo, diámetro, peso), bloque de autenticidad (foto del sello 925 y texto de garantía), costo y plazo de despacho, `button-primary` "Agregar al carrito" y `button-whatsapp`.

- El precio, el selector de talla y "Agregar al carrito" se ven sin hacer scroll en desktop.
- Las medidas siempre en milímetros, centímetros y gramos.

### Selector de talla (`size-selector`)

Botones cuadrados de 48px con la talla (12, 14, 16, 18) o el largo (40 cm, 45 cm, 50 cm). Uno seleccionado a la vez (fondo azul). Las tallas sin stock aparecen deshabilitadas y tachadas, nunca ocultas.

### Article card (`card-article`)

Foto 16:9, categoría en `text-secondary`, título en `title-sm` (máximo 3 líneas), extracto de 2 líneas, fecha y enlace "Leer artículo". Hover: sombra suave y título en azul.

### Review card (`card-review`)

Cinco estrellas en bronce, comentario entre comillas, nombre y comuna de la clienta ("Valentina, Viña del Mar") y, si existe, foto real de la pieza puesta.

### Beneficios (`benefit-item`)

Fila de 4 ítems con ícono y texto corto: "Plata ley 925 certificada", "Joyas con garantía", "Despacho a todo Chile con seguimiento" y "Atención por WhatsApp".

### Formulario de leads (`lead-form`)

Bloque azul con título "Recibe novedades y recordatorios para regalar", campo de correo, campo opcional de WhatsApp, casilla de consentimiento y `button-secondary` "Quiero recibirlos". Máximo 2 campos obligatorios.

### Campos de formulario (`input-field`)

Etiqueta visible siempre encima del campo (nunca solo placeholder). Estados: foco (borde azul de 2px), error (borde y `message-error` debajo, por ejemplo "Escribe un correo válido") y disabled.

### Resumen del carrito (`cart-summary`)

Subtotal, despacho según comuna (selector de comuna y plazo estimado), total, `button-primary` "Ir a pagar", texto "Compra sin crear cuenta · Webpay o transferencia" y enlace "Seguir comprando". Sin cuentas regresivas, códigos de invitación ni servicios extra.

### Footer (`footer`)

Enlaces a Tienda, Blog, Contacto, Preguntas frecuentes, Garantía y autenticidad, Guía de tallas, Despacho y cambios, Términos y condiciones y Política de privacidad; redes sociales; medios de pago (solo Webpay y transferencia) y un único WhatsApp chileno (+56 9 XXXX XXXX). Fondo azul `primary` y los mismos enlaces en todas las pantallas.

## Do's and Don'ts

**Do**

- Mostrar "plata ley 925" en cada producto, ficha y en la barra de confianza.
- Escribir precios en pesos chilenos con formato $29.990.
- Usar un tono cercano y claro, en español de Chile, con tuteo ("Elige tu talla", "Te respondemos hoy").
- Mostrar el costo y plazo del despacho antes de pagar.
- Usar fotos reales de las piezas, sobre fondo blanco o en uso.
- Mantener el mismo navbar y footer en todas las pantallas.

**Don't**

- No mencionar oro, platino, diamantes, certificados GIA ni "inversión".
- No usar lenguaje de alta joyería exclusiva ("Haute Joaillerie", "Atelier privado").
- No inventar cifras ni historia del negocio (años de trayectoria, cantidad de clientas, fundadores).
- No usar el gris plata como color de texto ni el bronce como fondo de botones principales.
- No poner más de un `button-primary` por sección.
- No usar ventanas emergentes al entrar al sitio ni cuentas regresivas.
- No inventar plazos de garantía, días de cambio ni políticas que no estén en el brief.
- No agregar medios de pago distintos de Webpay y transferencia.
- No cambiar el navbar ni el footer entre pantallas.
- No usar fotos con interfaces, capturas de otros sitios ni texto encima.
- No usar marcadores entre corchetes como [Título] o [$XX.XXX]; siempre textos reales.
- No agregar en mobile una barra de navegación inferior; la navegación va en el menú hamburguesa.
- No reemplazar el logo del header por un título de pantalla en mobile.
- No usar más de un h1 por pantalla; el header nunca usa h1.
