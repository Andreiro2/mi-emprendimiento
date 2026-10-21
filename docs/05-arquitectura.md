# Arquitectura de la información — Joyas Kofran

> Guía: [Arquitectura de la información](../evaluacion/guias/fase-1-requerimientos/05-arquitectura.md)

## Mapa de sitio

```text
Inicio (landing)
├── Tienda
│   ├── Categoría: Anillos
│   ├── Categoría: Cadenas y collares
│   ├── Categoría: Aros
│   ├── Categoría: Pulseras
│   ├── Categoría: Dijes
│   ├── Ficha de producto
│   └── Carrito
├── Blog
│   ├── Categoría: Cuidado y duración de la plata
│   ├── Categoría: Cómo elegir bien
│   ├── Categoría: Regalos e ideas
│   └── Artículo
├── Garantía y autenticidad
├── Guía de tallas
├── Despacho y cambios
├── Contacto
├── Preguntas frecuentes
├── Términos y condiciones
├── Política de privacidad
└── 404
```

Las categorías de la tienda y del blog no son páginas distintas: en el prototipo son la misma pantalla de tienda o de blog, filtrada.

## User flows

> Guía: [User flow](../evaluacion/guias/fase-1-requerimientos/06-user-flow.md)

### Flujo 1: compra

**Punto de entrada:** Camila ve una joya en una historia o publicación de Instagram, toca el enlace y aterriza directo en la ficha del producto, desde el celular y de noche. No pasa por el inicio.
**Meta:** llegar al Carrito con la pieza y la talla elegidas.

```text
Instagram (historia o publicación de una joya)
→ Ficha de producto
→ [Mira fotos, precio, medidas y sello 925]
◇ ¿Tiene dudas?
   ├── Sí → [Elige qué resolver]
   │     ├── Autenticidad o garantía → Garantía y autenticidad
   │     │     → [Lee que es plata ley 925 y cómo funciona la garantía]
   │     │     → [Vuelve a la ficha de producto]
   │     ├── Talla → Guía de tallas
   │     │     → [Compara su medida con la tabla de largos y anillos]
   │     │     → [Vuelve a la ficha de producto]
   │     └── Despacho o cambios → Despacho y cambios
   │           → [Revisa costo y plazo para su zona y la política de cambio]
   │           ◇ ¿El plazo calza con su fecha?
   │              ├── Sí → [Vuelve a la ficha de producto]
   │              └── No → Fin: sale del sitio
   └── No → continúa
→ [Elige variante (talla o largo)]
◇ ¿Qué decide?
   ├── Consultar por WhatsApp → WhatsApp (mensaje de la pieza ya escrito) → Fin
   ├── Seguir mirando → [Clic en "Seguir mirando"] → Tienda
   └── Agregar al carrito → [Clic en "Agregar al carrito"]
→ Carrito
→ [Ve la pieza y la talla elegidas]
→ Fin: carrito con la pieza y la talla elegidas
   (si quiere seguir comprando → Tienda; continuar al pago queda fuera del alcance de este flujo)
```

### Flujo 2: contenido

**Punto de entrada:** Camila busca en Google algo como "por qué se oscurece la plata 925" y aterriza directo en un artículo del blog sobre el cuidado de la plata. Esto responde a su frustración con joyas que cambian de color.
**Meta:** llegar a una ficha de producto, al formulario de contacto o a WhatsApp.

```text
Google ("por qué se oscurece la plata 925")
→ Artículo: "Por qué se oscurece la plata 925 y cómo limpiarla en casa sin dañarla"
→ [Lee los consejos de cuidado]
◇ ¿Quiere más confianza antes de decidir?
   ├── Sí → [Clic en el enlace del artículo] → Garantía y autenticidad
   │     → [Lee cómo se respalda la calidad]
   │     → [Vuelve al artículo]
   └── No → continúa
→ [Llega al final del artículo y ve las piezas mencionadas y las opciones de contacto]
◇ ¿Qué decide?
   ├── Ver una pieza → [Clic en la pieza mencionada] → Ficha de producto
   │     → [Revisa la pieza]
   │     → Fin: meta alcanzada (puede continuar al Flujo 1 desde la elección de variante)
   ├── Quedar en contacto → Contacto
   │     → [Deja su correo o WhatsApp en el formulario para recibir novedades o consejos]
   │     → Fin: lead captado
   ├── Preguntar → WhatsApp → Fin
   └── Seguir leyendo → Blog (listado)
         → [Busca otro artículo y elige uno]
         → vuelve al inicio del flujo con otro artículo
```

## Categorías

> Guía: [Categorías de productos y temas del blog](../evaluacion/guias/fase-1-requerimientos/07-categorias.md)

### Categorías de productos

Se agrupan por **tipo de pieza**. La agrupación por momento o intención de compra (para mí, todos los días; para regalar; para ocasiones especiales como cumpleaños, aniversarios y fechas del año) funciona como **filtro** de la tienda, no como categoría.

| Categoría | Productos |
|---|---|
| Anillos | Argollas y anillos de plata ley 925 |
| Cadenas y collares | Cadenas finas y collares de plata ley 925 |
| Aros | Aros pequeños y argollas de plata ley 925 |
| Pulseras | Pulseras de plata ley 925 |
| Dijes | Dijes de plata ley 925 |

### Categorías del blog

| Categoría | Idea de artículo | Necesidad o motivación de la proto-persona | Producto relacionado |
|---|---|---|---|
| Cuidado y duración de la plata | "Por qué se oscurece la plata 925 y cómo limpiarla en casa sin dañarla" | Su miedo a que la joya cambie de color a las pocas semanas y a no saber cómo cuidarla | Cadenas y collares finos de uso diario, que son los que más contacto tienen con la piel |
| Cómo elegir bien | "Cómo medir tu dedo en casa y no equivocarte con la talla de un anillo" | No quiere errar la talla al comprar online y no poder cambiarla | Anillos, con enlace a la guía de tallas y a la política de cambio |
| Regalos e ideas | "Regalos de plata 925 según tu presupuesto: ideas desde $20.000 hasta $60.000" | Quiere quedar bien con un regalo que parezca pensado, sin pasarse del presupuesto ni improvisar a último minuto | Aros y dijes en cada tramo de precio |
