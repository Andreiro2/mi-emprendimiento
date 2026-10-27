# Spec de desarrollo — Joyas Kofran

> Guía: [Spec de desarrollo](../evaluacion/guias/fase-2-specs/07-spec-de-desarrollo.md)

## Insumos y prompt para el asistente 

```text
Lee DESIGN.md, docs/09-spec-diseno.md y docs/10-spec-desarrollo.md.
Para el contexto del negocio y la usuaria, lee también docs/01-brief.md,
docs/02-proto-personas.md, docs/05-arquitectura.md y las capturas de
docs/img/ (wireframes y prototipo).
En la carpeta stitch/ está el código exportado de Stitch de cada pantalla.
Construye el sitio siguiendo exactamente docs/10-spec-desarrollo.md:
solo HTML y CSS, la estructura de archivos y la navegación definidas,
las variables de :root con los valores de DESIGN.md y la estructura
semántica de cada página. Usa el código de Stitch solo como referencia
visual. Al terminar, revisa cada criterio de aceptación y dime cuáles
se cumplen y cuáles no.
```

## 1. Estructura de archivos

```text
joyas-kofran/
├── index.html            # Landing
├── tienda.html           # Catálogo de productos con filtros (visuales)
├── producto.html         # Detalle de un producto
├── carrito.html          # Carrito (prototipo visual con productos de ejemplo)
├── blog.html             # Listado de artículos
├── articulo.html         # Artículo del blog
├── contacto.html         # Contacto, formulario de leads y datos de la tienda
├── garantia.html         # Garantía y autenticidad (sello 925, certificado)
├── guia-tallas.html      # Tablas de largos de cadena y tallas de anillo
├── despacho.html         # Costos y plazos por zona, cambios y devoluciones
├── preguntas-frecuentes.html
├── terminos.html         # Términos y condiciones
├── privacidad.html       # Política de privacidad
├── 404.html              # Página no encontrada (GitHub Pages la usa sola)
├── css/
│   ├── variables.css     # :root con colores, tipografía y espaciado
│   ├── base.css          # Reset, tipografía, enlaces, botones, formularios
│   ├── layout.css        # Header, footer, grillas y contenedores
│   ├── components.css    # Tarjetas, etiquetas, menú, carrito, reseñas
│   └── responsive.css    # Media queries (tablet y desktop)
├── img/                  # Imágenes optimizadas (.webp o .jpg) con nombres descriptivos
├── stitch/               # Código exportado de Stitch (solo referencia visual)
├── docs/                 # Documentación de las fases 1 y 2
└── DESIGN.md
```

## 2. Páginas y navegación

| Desde | Elemento | Lleva a |
|---|---|---|
| Todas las páginas | Logo Joyas Kofran | `index.html` |
| Todas las páginas | Menú "Tienda" | `tienda.html` |
| Todas las páginas | Menú "Blog" | `blog.html` |
| Todas las páginas | Menú "Contacto" | `contacto.html` |
| Todas las páginas | Ícono de carrito | `carrito.html` |
| Todas las páginas | Botón flotante de WhatsApp | Enlace `https://wa.me/` al número del negocio (abre en pestaña nueva) |
| `index.html` | Botón "Ver colección" (hero) | `tienda.html` |
| `index.html` | Tarjeta de categoría | `tienda.html` |
| `index.html` | Tarjeta de producto destacado | `producto.html` |
| `index.html` | Tarjeta de artículo | `articulo.html` |
| `index.html` | Botón "Ver todos los artículos" | `blog.html` |
| `tienda.html` | Tarjeta de producto | `producto.html` |
| `producto.html` | Enlace "Ver guía de tallas" | `guia-tallas.html` |
| `producto.html` | Enlace "Ver garantía" | `garantia.html` |
| `producto.html` | Enlace "Ver despacho y cambios" | `despacho.html` |
| `producto.html` | Botón "Agregar al carrito" | `carrito.html` |
| `producto.html` | Enlace "Seguir mirando" | `tienda.html` |
| `producto.html` | Botón "Consultar por WhatsApp" | Enlace `https://wa.me/` (pestaña nueva) |
| `carrito.html` | Botón "Ir a pagar" | `contacto.html` (en el prototipo no hay pasarela de pago) |
| `carrito.html` | Enlace "Seguir comprando" | `tienda.html` |
| `blog.html` | Tarjeta de artículo | `articulo.html` |
| `articulo.html` | Tarjeta de "Piezas mencionadas" | `producto.html` |
| `articulo.html` | Enlace en el texto "Garantía y autenticidad" | `garantia.html` |
| `articulo.html` | Botón "Ir a contacto" | `contacto.html` |
| `articulo.html` | Botón "Consultar por WhatsApp" | Enlace `https://wa.me/` (pestaña nueva) |
| `articulo.html` | Enlace "Volver al blog" | `blog.html` |
| `contacto.html` | Enlace de correo | `mailto:` con el correo del negocio |
| Footer (todas) | Enlaces a Tienda, Blog y Contacto | `tienda.html`, `blog.html`, `contacto.html` |
| Footer (todas) | Preguntas frecuentes, Garantía y autenticidad, Guía de tallas, Despacho y cambios | `preguntas-frecuentes.html`, `garantia.html`, `guia-tallas.html`, `despacho.html` |
| Footer (todas) | Términos y condiciones, Política de privacidad | `terminos.html`, `privacidad.html` |
| `404.html` | Botones "Ir al inicio" e "Ir a la tienda" | `index.html`, `tienda.html` |
| Footer (todas) | Redes sociales | URL externa de cada red (pestaña nueva, `rel="noopener"`) |

Todos los enlaces internos usan rutas relativas (por ejemplo `tienda.html`, no `/tienda.html`), para que funcionen en GitHub Pages dentro de la carpeta del repositorio.

## 3. Estructura semántica

**Estructura común a todas las páginas**
- `<html lang="es">`, `<meta charset="utf-8">`, `<meta name="viewport" content="width=device-width, initial-scale=1">` y un `<title>` único por página.
- Enlace "Saltar al contenido" al inicio, que apunta a `#contenido`.
- `<header>` con el logo y `<nav aria-label="Principal">`, con una lista `<ul>` de enlaces. El enlace de la página actual lleva `aria-current="page"`.
- `<main id="contenido">` con un solo `<h1>` por página.
- `<footer>` con `<nav aria-label="Pie de página">`, datos de contacto y redes sociales.
- Jerarquía de títulos sin saltos: h1 → h2 → h3.
- Todas las imágenes llevan `alt` descriptivo. Las decorativas usan `alt=""`.

**index.html**
- `<main>` con las secciones: hero (h1 con la propuesta de valor y botón), categorías, productos destacados, beneficios (plata ley 925, garantía, atención), reseñas y artículos recientes del blog.
- Cada sección es un `<section>` con su propio `<h2>`.
- Las reseñas usan `<blockquote>` con el nombre del cliente en `<cite>`.

**tienda.html**
- `<h1>` "Tienda" y un bloque de filtros (`<form>` con `<fieldset>` y `<legend>`) que en el prototipo es solo visual.
- Lista de productos en `<ul>`, con una tarjeta `<article>` por producto: `<img>`, `<h2>` con el nombre, precio en `<p>` y enlace al detalle.

**producto.html**
- `<h1>` con el nombre del producto, galería de imágenes y precio.
- Descripción, material (plata ley 925) y garantía en `<section>`.
- Botones "Agregar al carrito" y "Consultar por WhatsApp".

**carrito.html**
- `<h1>` "Carrito" y una tabla `<table>` con `<caption>`, encabezados `<th scope="col">` y una fila por producto de ejemplo.
- Resumen del pedido en `<aside>` con selector de comuna, despacho, total y el botón "Ir a pagar".

**blog.html**
- `<h1>` "Blog" y lista de artículos en `<ul>`. Cada tarjeta es un `<article>` con imagen, categoría, `<h2>`, extracto y fecha en `<time datetime="">`.

**articulo.html**
- `<article>` con `<h1>`, fecha en `<time>`, imagen principal con `<figure>` y `<figcaption>`, y el contenido dividido con `<h2>` y `<h3>`.
- `<aside>` con "Piezas mencionadas" y botones de WhatsApp y contacto.

**contacto.html**
- `<h1>` "Contacto" y un `<form>` con `<label for>` asociado a cada `<input>` y `<textarea>`, con los atributos `required` y `type` correctos (`email`, `tel`).
- Datos de contacto en `<address>`.

**garantia.html, guia-tallas.html, despacho.html, preguntas-frecuentes.html, terminos.html y privacidad.html**
- `<h1>` con el nombre de la página y el contenido en `<section>` con `<h2>`. Las tablas de tallas y despacho usan `<table>` con `<caption>` y `<th scope="col">`. Las preguntas frecuentes usan `<details>` y `<summary>`.

**404.html**
- `<h1>` "No encontramos esta página", un texto corto y dos enlaces: inicio y tienda.

## 4. Organización del CSS

Los archivos se enlazan en este orden desde el `<head>` de cada página: `variables.css`, `base.css`, `layout.css`, `components.css` y `responsive.css`. Los estilos se escriben mobile first, con `min-width` en los media queries.

Breakpoints: mobile hasta 767px, tablet de 768px a 1023px y desktop desde 1024px.

```css
:root {
  /* los valores salen de DESIGN.md */

  /* Colores */
  --color-primary: #1F4E79;
  --color-primary-hover: #183E60;
  --color-on-primary: #FFFFFF;
  --color-secondary: #C9CDD3;
  --color-on-secondary: #1C1C1E;
  --color-tertiary: #8C5F22;
  --color-tertiary-hover: #6F4A1A;
  --color-on-tertiary: #FFFFFF;
  --color-neutral: #FAF8F5;
  --color-surface: #FFFFFF;
  --color-on-surface: #1C1C1E;
  --color-on-surface-variant: #5C5C5C;
  --color-disabled: #D6D6D6;
  --color-on-disabled: #4A4A4A;
  --color-success: #2E7D4F;
  --color-error: #B3261E;

  /* Tipografía */
  --font-heading: "Cormorant Garamond", Georgia, serif;
  --font-body: "Inter", Arial, sans-serif;
  --fs-h1: 3rem;        /* 48px desktop, 2rem (32px) en mobile */
  --fs-h2: 2.25rem;     /* 36px desktop, 1.625rem (26px) en mobile */
  --fs-h3: 1.5rem;      /* 24px desktop, 1.25rem (20px) en mobile */
  --fs-body: 1rem;      /* 16px */
  --fs-title-sm: 1rem;  /* 16px, nombre en tarjetas */
  --fs-price: 1.125rem; /* 18px */
  --fs-small: 0.875rem; /* 14px */
  --fs-tag: 0.8125rem;  /* 13px */
  --fs-button: 1rem;    /* 16px */
  --ls-button: 0.5px;
  --lh-heading: 1.2;
  --lh-body: 1.6;

  /* Espaciado */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;
  --space-3xl: 64px;

  /* Forma */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-full: 9999px;

  /* Layout */
  --container-max: 1200px;
  --gutter: 16px;       /* 24px en tablet y 32px en desktop */
  --filters-width: 240px;
  --touch-min: 44px;

  /* Elevación */
  --border-card: 1px solid var(--color-secondary);
  --shadow-hover: 0 4px 12px rgba(31, 78, 121, 0.12);
  --overlay: rgba(28, 28, 30, 0.5);
}
```

**Componentes del DESIGN.md y su clase CSS**

| Token en `DESIGN.md` | Clase CSS |
|---|---|
| `navbar` / `footer` / `trust-bar` | `.cabecera` / `.pie` / `.barra-confianza` |
| `button-primary` / `button-secondary` / `button-whatsapp` | `.boton-primario` / `.boton-secundario` / `.boton-whatsapp` |
| `tag-925` | `.etiqueta-925` |
| `chip-filter` / `search-bar` | `.chip-filtro` / `.buscador` |
| `card-product` / `card-category` / `card-article` / `card-review` | `.tarjeta-producto` / `.tarjeta-categoria` / `.tarjeta-articulo` / `.tarjeta-resena` |
| `size-selector` / `price` | `.selector-talla` / `.precio` |
| `input-field` / `lead-form` / `cart-summary` | `.campo-formulario` / `.formulario-leads` / `.resumen-carrito` |
| `message-success` / `message-error` / `benefit-item` | `.mensaje-exito` / `.mensaje-error` / `.beneficio` |

Los estados del `DESIGN.md` se traducen así: `-hover` → `:hover`, `-active` → `:active` o `[aria-pressed="true"]` / `:checked`, `-disabled` → `:disabled` o `[aria-disabled="true"]`.

**Convenciones**
- Los colores, tamaños de fuente y espaciados se usan siempre con `var(--...)`. No se escriben valores sueltos en los demás archivos.
- Nombres de clases en español y minúsculas, con guiones (`tarjeta-producto`, `boton-primario`, `etiqueta-oferta`).
- Una clase por componente, según la tabla anterior.
- Estados `:hover`, `:focus-visible` y `:disabled` definidos para botones, enlaces e inputs. El foco visible usa un contorno de 2px con `--color-tertiary`.
- Las fuentes se cargan desde Google Fonts con `<link>` en el `<head>` y `font-display: swap`.
- No se usa JavaScript. El menú móvil se resuelve solo con CSS (checkbox y `label`).

## 5. Criterios de aceptación

**Navegación**
- [ ] Existen los 14 archivos HTML definidos y se abren sin errores 404 en GitHub Pages (salvo `404.html`, que aparece al escribir una URL inexistente).
- [ ] Todos los enlaces de la tabla de la sección 2 llevan al destino indicado.
- [ ] El menú principal aparece igual en todas las páginas y marca la página actual con `aria-current="page"`.
- [ ] Desde cualquier página se llega al carrito y a WhatsApp en un clic.
- [ ] Los enlaces externos (WhatsApp, redes sociales) abren en pestaña nueva con `rel="noopener"`.

**Funcionalidades**
- [ ] Flujo de compra: tienda → producto → carrito se puede recorrer solo con enlaces.
- [ ] Flujo de contenido: blog → artículo → producto relacionado o contacto funciona completo.
- [ ] El menú móvil se abre y se cierra solo con CSS.
- [ ] El botón de WhatsApp abre una conversación con el número del negocio y, en la ficha, con el nombre de la pieza ya escrito.
- [ ] Todos los precios están en pesos chilenos con formato $29.990 y la palabra "plata 925" aparece en cada tarjeta de producto.
- [ ] La ficha muestra medidas, sello 925, garantía y costo de despacho antes del botón "Agregar al carrito".
- [ ] El formulario de contacto muestra validación del navegador (`required`, `type="email"`). El envío real queda como prototipo visual, porque no hay backend.
- [ ] Las funciones que requieren servidor (filtros reales, carrito dinámico, pago) están diseñadas pero se indican como prototipo visual.

**Diseño**
- [ ] Todos los colores y tamaños vienen de las variables de `:root`, sin valores sueltos.
- [ ] Los colores y las fuentes coinciden con `DESIGN.md` y con `docs/08-color-tipografia.md` (principal `#1F4E79`, Cormorant Garamond e Inter).
- [ ] Los botones, tarjetas, etiquetas e inputs usan los mismos estilos en todas las páginas.
- [ ] Los botones tienen estados hover, foco y deshabilitado.
- [ ] El diseño se parece a las pantallas de Stitch en estructura y estilo.

**Responsive**
- [ ] No hay scroll horizontal a 360px, 768px y 1280px de ancho.
- [ ] En mobile las grillas pasan a 1 columna y el menú se colapsa.
- [ ] En tablet las tarjetas se muestran en 2 columnas y en desktop en 3 (4 en la landing).
- [ ] En mobile el botón "Agregar al carrito" queda fijo abajo y el botón flotante de WhatsApp no lo tapa.
- [ ] Los títulos usan los tamaños mobile y desktop definidos en `docs/08-color-tipografia.md`.
- [ ] Las imágenes se adaptan al ancho (`max-width: 100%`) y no se deforman.
- [ ] Los botones y enlaces táctiles miden al menos 44×44px.

**Accesibilidad y publicación**
- [ ] Cada página tiene un solo `<h1>` y una jerarquía de títulos sin saltos.
- [ ] Todas las imágenes tienen `alt` y los campos de formulario tienen `<label>`.
- [ ] El contraste de texto cumple WCAG AA (mínimo 4,5:1).
- [ ] Se puede navegar con teclado y el foco es visible en todos los elementos interactivos.
- [ ] El HTML valida en el validador del W3C sin errores.
- [ ] El sitio está publicado en GitHub Pages y la URL funciona.
- [ ] El repositorio incluye un `README.md` con la URL publicada y las instrucciones para ejecutarlo.
