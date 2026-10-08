# Tecnologías del proyecto — Joyas Kofran

Restricciones
Sin JavaScript no hay lógica. No se pueden hacer cálculos, recordar nada entre visitas ni reaccionar a lo que escribe el usuario.
GitHub Pages es hosting estático. No hay servidor ni base de datos, así que nada se guarda: ni comentarios, ni favoritos, ni pedidos.
El repositorio es público en el plan gratuito. Cualquier clave o dato que pongas en el código lo puede ver cualquiera.
Política de uso: GitHub Pages no está pensado ni permitido para operar un negocio online o una tienda de comercio electrónico, ni sitios dirigidos principalmente a facilitar transacciones comerciales, y tampoco debe usarse para datos sensibles como números de tarjeta. Si el sitio es un prototipo académico, no hay problema. Si quieres vender de verdad desde ahí, necesitas cambiar de hosting o de plataforma. 
github
Límites de tamaño: el sitio publicado no puede superar 1 GB y hay un límite blando de 100 GB de transferencia al mes. Las fotos de joyas deben ir optimizadas. 
github
Filtros solo con CSS: dependen de selectores modernos como :has(), que no funcionan en navegadores antiguos.
Mantenimiento manual: cada producto se edita a mano en el código. Con un catálogo grande se vuelve inmanejable.
Los formularios dependen de terceros: el envío y el almacenamiento de datos lo hace otro servicio, así que necesitas aviso de privacidad y consentimiento.
✅ Funcionan de verdad solo con HTML y CSS
Funcionalidad	Cómo funciona hoy	Integración en versión real (y para qué)
Filtrar (solo catálogo chico)	Botones de opción + CSS que muestran u ocultan piezas por categoría o precio.	Filtros con JavaScript, para combinar criterios y soportar un catálogo que crece.
Compartir	Enlaces fijos a WhatsApp, Facebook, X y correo con la URL de cada página ya escrita. Instagram no tiene enlace web de compartir.	API nativa de compartir del celular (requiere JavaScript), para abrir el menú de apps del teléfono.
2. Guía de talla	Página estática con tabla de largos de cadena y diámetros de anillo.	Una calculadora (JavaScript), para que la usuaria mida su dedo y obtenga la talla sin interpretar tablas.
3. Autenticidad y garantía	Páginas fijas con política de garantía y cambio, foto del sello 925 y certificado en PDF descargable.	Código único por pieza con verificación en una base de datos, para comprobar cada joya individual.
5. WhatsApp con contexto	Un enlace wa.me por producto con el mensaje ya escrito ("Hola, me interesa [pieza]").	WhatsApp Business API, solo si necesitas respuestas automáticas o varios agentes.
8. Del blog a los productos	Enlaces internos entre artículos y fichas. Los consejos de cuidado van en una página que enlazas con un QR en la tarjeta del paquete.	Correo automático postventa (Brevo o Mailchimp), para enviar el cuidado de la plata sin depender del QR.
🟡 Funcionan parcialmente o con un servicio externo
Funcionalidad	Qué sí funciona	Qué falta / integración real
Captar leads	Un formulario HTML cuyo envío lo recibe Formspree, Google Forms, Brevo o Mailchimp.	Protección anti-spam y consentimiento. La lista de contactos vive en el servicio externo, no en tu sitio.
Seleccionar (variante o talla)	Los botones de opción permiten elegir, pero la elección no viaja a ninguna parte.	Un carrito o un formulario con JavaScript. Mientras tanto, un enlace de WhatsApp por cada variante.
4. Despacho y seguimiento	Tabla estática de costos y plazos por zona o comuna, y enlaces a las páginas de seguimiento de Starken, Chilexpress o Correos de Chile.	Cálculo por comuna y seguimiento dentro del sitio requieren API del courier y un servidor, o una plataforma de tienda que ya lo incluya.
6. Regalos por ocasión y presupuesto	Páginas curadas a mano ("Regalos hasta $30.000", "Para mamá"). El mensaje de regalo se pide por WhatsApp.	Un asistente interactivo y mensaje de regalo dentro del pedido requieren JavaScript y un sistema de pedidos.
7. Compra sin cuenta con medios de pago	Un link de pago por producto (los ofrecen servicios como Mercado Pago, Flow o Khipu; verifica disponibilidad y comisiones) y transferencia con comprobante por WhatsApp.	No hay carrito, stock ni confirmación automática. Una versión real necesita una plataforma de e-commerce (Shopify, Tiendanube, WooCommerce), y eso además resuelve la restricción de GitHub Pages.
🔴 Solo prototipo visual
Funcionalidad	Por qué no funciona	Integración en versión real (y para qué)
Buscar	Sin JavaScript no se puede buscar dentro del sitio. Un formulario hacia Google con site: funciona, pero saca a la usuaria de tu página.	Pagefind o Lunr (JavaScript) para buscar en un sitio estático, o el buscador integrado de la plataforma de tienda.
Comentar	No hay dónde guardar lo que escriben.	Reseñas de la plataforma de tienda. Giscus o Disqus exigen cuenta y no calzan con Camila. Alternativa manual: formulario de reseña que tú revisas y pegas en el HTML.
1. Guardar favoritos	Requiere recordar estado entre visitas.	localStorage con JavaScript para guardar en el mismo dispositivo, o cuentas de usuario (Firebase o Supabase) para recuperarlos desde otro.
Resumen y siguiente paso

De 14 funcionalidades, 6 funcionan de verdad, 5 funcionan a medias o con un servicio externo y 3 quedan como prototipo. Para presentarlo como prototipo, rotula en cada ficha lo que es maqueta, sobre todo el pago, los comentarios y los favoritos, para no prometer lo que el sitio no hace.

Si quieres pasar a una versión real, el cambio que más funcionalidades resuelve de una vez (pago, carrito, stock, búsqueda, reseñas, despacho) es una plataforma de tienda. Tu sitio de HTML y CSS quedaría como landing y blog.
