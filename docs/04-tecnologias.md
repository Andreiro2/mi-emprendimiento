# Tecnologías del proyecto — Joyas Kofran

> Guía: [Tecnologías del proyecto](../evaluacion/guias/fase-1-requerimientos/04-tecnologias.md)

## Stack

| Área | Herramienta | Para qué la uso |
|---|---|---|
| Construcción | HTML + CSS | Maquetar la landing, el blog y la tienda de Joyas Kofran sin frameworks ni gestor de contenido |
| Versionado | Git y GitHub | Guardar el avance con commits y tener el proyecto y la documentación en la nube |
| Publicación | GitHub Pages | Publicar el sitio gratis con una URL pública, como prototipo académico |
| Diseño | Whimsical | Armar el moodboard, calcar los componentes y hacer los wireframes |
| Diseño | Google Stitch | Generar el prototipo referencial en alta fidelidad (desktop y mobile) a partir de mis specs |
| IA | ChatGPT y Claude | Generar ideas iniciales, ordenar la estructura del sitio y revisar mis documentos |
| Editor | Visual Studio Code | Escribir, organizar y editar el código HTML y CSS del sitioweb |

## Qué es funcional y qué es prototipo

Los estados son tres: **Funcional** (funciona de verdad solo con HTML y CSS), **Parcial** (funciona con ayuda de un servicio externo o solo en parte) y **Prototipo visual** (se ve, pero no procesa ni guarda datos).

| Funcionalidad | Estado en esta versión |
|---|---|
| Navegar los artículos por categoría y pasar del blog a las fichas de producto | Funcional (enlaces internos entre páginas) |
| Filtrar productos por categoría o precio | Funcional solo con catálogo chico (botones de opción + CSS; requiere navegadores modernos con `:has()`) |
| Ver el detalle de un producto | Funcional (ficha estática) |
| Compartir un artículo | Funcional (enlaces fijos a WhatsApp, Facebook, X y correo; Instagram no tiene enlace web de compartir) |
| Guía de talla (largo de cadena, diámetro de anillo, peso) | Funcional (página estática con tablas) |
| Autenticidad 925 y garantía | Funcional (páginas fijas con política de garantía y cambio, foto del sello y certificado en PDF descargable) |
| Consultar por WhatsApp sobre una pieza | Funcional (enlace `wa.me` por producto con el mensaje ya escrito) |
| Consejos de cuidado de la plata | Funcional (página enlazada con un QR en la tarjeta del paquete) |
| Captar leads | Parcial (formulario HTML cuyo envío recibe Formspree, Google Forms, Brevo o Mailchimp; la lista vive en el servicio externo) |
| Seleccionar variante o talla | Parcial (los botones permiten elegir, pero la elección no viaja a ninguna parte) |
| Despacho y seguimiento | Parcial (tabla estática de costos y plazos por comuna y enlaces a Starken, Chilexpress o Correos de Chile) |
| Regalos por ocasión y presupuesto | Parcial (páginas curadas a mano como "Regalos hasta $30.000" o "Para mamá"; el mensaje de regalo se pide por WhatsApp) |
| Compra sin cuenta con medios de pago | Parcial (link de pago por producto y transferencia con comprobante por WhatsApp; sin carrito, stock ni confirmación automática) |
| Agregar al carrito | Prototipo visual |
| Buscar productos | Prototipo visual (sin JavaScript no se puede buscar dentro del sitio) |
| Comentar un artículo | Prototipo visual (no hay dónde guardar lo que escriben) |
| Guardar favoritos | Prototipo visual (requiere recordar estado entre visitas) |

## Integraciones para una versión real

- **Plataforma de e-commerce (Shopify, Tiendanube o WooCommerce):** carrito, stock, pagos con confirmación automática, seguimiento de pedidos y reseñas. Además resuelve la restricción de GitHub Pages, que no permite operar una tienda.
- **Pasarela de pago (Webpay, Mercado Pago, Flow o Khipu):** cobrar con tarjeta o transferencia sin salir del sitio (verificar disponibilidad y comisiones).
- **JavaScript:** filtros combinables para un catálogo que crece, calculadora de talla, API nativa de compartir del celular y favoritos con `localStorage`.
- **Buscador (Pagefind o Lunr):** buscar dentro de un sitio estático, o el buscador integrado de la plataforma de tienda.
- **Cuentas de usuario (Firebase o Supabase):** recuperar favoritos desde otro dispositivo.
- **API del courier y servidor:** calcular el despacho por comuna y mostrar el seguimiento dentro del sitio, o una plataforma de tienda que ya lo incluya.
- **Código único por pieza con base de datos:** verificar la autenticidad de cada joya individual.
- **WhatsApp Business API:** respuestas automáticas o varios agentes, solo si se necesita.
- **Email marketing (Brevo o Mailchimp):** guardar los contactos y enviar automáticamente el cuidado de la plata después de comprar, sin depender del QR.
- **Reseñas:** las de la plataforma de tienda, o un formulario de reseña que reviso y publico a mano. Giscus y Disqus exigen cuenta y no calzan con la proto-persona.

## Restricciones

- **Plazo:** 29 de septiembre al 14 de octubre de 2026 (Fase 1 el 5 de octubre, Fase 2 el 12 y Fase 3 el 14).
- **Marca:** no hay manual de marca previo; la identidad visual se define en la Fase 2.
- **Dispositivos:** el sitio debe funcionar en celular y escritorio, priorizando el celular porque Camila navega casi solo desde el teléfono.
- **Sin lógica ni datos:** sin JavaScript no hay cálculos, memoria entre visitas ni reacción a lo que escribe el usuario, y GitHub Pages es hosting estático: no hay servidor ni base de datos, así que no se guardan comentarios, favoritos ni pedidos.
- **Repositorio público:** cualquier clave o dato que se ponga en el código lo puede ver cualquiera.
- **Política de uso de GitHub Pages:** no está permitido para operar un negocio online ni para datos sensibles como números de tarjeta. Como prototipo académico no hay problema; para vender de verdad hay que cambiar de hosting o de plataforma.
- **Tamaño:** el sitio publicado no puede superar 1 GB y hay un límite blando de 100 GB de transferencia al mes, por lo que las fotos de las joyas deben ir optimizadas.
- **Mantenimiento manual:** cada producto se edita a mano en el código, lo que se vuelve inmanejable con un catálogo grande.
- **Formularios de terceros:** el envío y almacenamiento de datos lo hace otro servicio, por lo que se necesita aviso de privacidad y consentimiento.
