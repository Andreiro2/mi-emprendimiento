# Arquitectura de la información — Joyas Kofran

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## Mapa de sitio

<!-- Incluye landing, blog, tienda y las páginas obligatorias:
contacto, preguntas frecuentes, términos, privacidad y 404. -->

```text
Inicio (landing)
├── Tienda
├── Blog
└── ...
```

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: compra

Flujo 1: Compra (hasta el carrito)

Punto de entrada: Camila ve una joya en una historia o publicación de Instagram, toca el enlace y aterriza directo en la ficha del producto, desde el celular y de noche. No pasa por el inicio.
Meta: llegar al Carrito con la pieza y la talla elegidas.

#	Pantalla	Acción de Camila	Decisión
1	Ficha de producto	Mira fotos, precio, medidas y sello 925.	Si tiene dudas, sigue a 2, 3 o 4. Si no, pasa a 5.
2	Garantía y autenticidad	Lee que es plata ley 925 y cómo funciona la garantía. Vuelve a la ficha.	Si queda tranquila, regresa al paso 1.
3	Guía de tallas	Compara su medida con la tabla de largos y anillos. Vuelve a la ficha.	Si ya sabe su talla, regresa al paso 1.
4	Despacho y cambios	Revisa costo y plazo para su zona y la política de cambio. Vuelve a la ficha.	Si el plazo no calza con su fecha, puede salir (fin del flujo).
5	Ficha de producto	Elige variante (talla o largo).	Agregar al carrito → paso 6. Consultar por WhatsApp → salida a WhatsApp con el mensaje de la pieza. Seguir mirando → Tienda.
6	Carrito	Ve la pieza y la talla elegidas.	Seguir comprando → Tienda. Continuar (fuera del alcance de este flujo).

### Flujo 2: contenido

Flujo 2: Contenido (del blog a un producto o contacto)

Punto de entrada: Camila busca en Google algo como "por qué se oscurece la plata 925" y aterriza directo en un artículo del blog sobre el cuidado de la plata. Esto responde a su frustración con joyas que cambian de color.
Meta: llegar a una ficha de producto, al formulario de contacto o a WhatsApp.

#	Pantalla	Acción de Camila	Decisión
1	Artículo del blog	Lee los consejos de cuidado.	Sigue a 2 si quiere más confianza, o decide en el paso 3.
2	Garantía y autenticidad	Entra desde un enlace del artículo y lee cómo se respalda la calidad. Vuelve al artículo.	Si queda convencida, regresa al paso 1 y avanza al 3.
3	Artículo del blog (final)	Llega al cierre, donde ve piezas mencionadas y opciones de contacto.	Ver una pieza → paso 4. Quedar en contacto → paso 5. Preguntar → WhatsApp. Seguir leyendo → Blog.
4	Ficha de producto	Revisa la pieza mencionada en el artículo.	Meta alcanzada. Desde aquí puede continuar al flujo de compra (paso 5 del Flujo 1).
5	Contacto	Deja su correo o WhatsApp en el formulario para recibir novedades o consejos.	Meta alcanzada.
6	Blog (listado)	Busca otro artículo.	Elige uno y vuelve al paso 1 con otro artículo.

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de productos

1. Dos formas de agrupar tus productos

Opción A: por tipo de pieza

Anillos
Cadenas y collares
Aros
Pulseras
Dijes

Opción B: por momento o intención de compra

Para mí, todos los días (básicos)
Para regalar
Para ocasiones especiales (cumpleaños, aniversarios, fechas del año)

### Categorías del blog

2. Tres categorías de blog

Todas parten de una necesidad de Camila y terminan enlazando a una ficha de producto, como en el flujo de contenido que definimos.

Categoría 1: Cuidado y duración de la plata

Artículo: "Por qué se oscurece la plata 925 y cómo limpiarla en casa sin dañarla".
Necesidad que atiende: su miedo a que la joya cambie de color a las pocas semanas y a no saber cómo cuidarla.
Producto enlazado: cadenas y collares finos de uso diario, que son los que más contacto tienen con la piel.

Categoría 2: Cómo elegir bien

Artículo: "Cómo medir tu dedo en casa y no equivocarte con la talla de un anillo".
Necesidad que atiende: que no quiere errar la talla al comprar online y no poder cambiarla.
Producto enlazado: anillos, con enlace a la guía de tallas y a la política de cambio.

Categoría 3: Regalos e ideas

Artículo: "Regalos de plata 925 según tu presupuesto: ideas desde $20.000 hasta $60.000" (ajusta los tramos a tus precios reales).
Necesidad que atiende: querer quedar bien con un regalo que parezca pensado, sin pasarse del presupuesto ni improvisar a último minuto.
Producto enlazado: aros y dijes en cada tramo de precio. Con la temporada de Navidad cerca, es un buen artículo para publicar pronto.
