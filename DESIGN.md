---
version: alpha
name: "[Joyas Kofran]"
description: "[Design system de Joyas Kofran en una línea]"
# Guía: evaluacion/guias/fase-2-specs/06-spec-de-diseno.md
# Reemplaza TODOS los valores de ejemplo por los de tu paleta y tipografía
# (docs/08-color-tipografia.md). Los HEX van siempre entre comillas.
# Valida con: npx @google/design.md lint DESIGN.md
colors:
  primary: "#1F4E79"
  primary-hover: "#183E60"
  on-primary: "#FFFFFF"
  secondary: "#E8EEF4"
  on-secondary: "#1A1A1A"
  tertiary: "#B5462B"
  on-tertiary: "#FFFFFF"
  neutral: "#FAFAFA"
  surface: "#FFFFFF"
  on-surface: "#1A1A1A"
  on-surface-variant: "#5C5C5C"
  disabled: "#D6D6D6"
  on-disabled: "#4A4A4A"
  error: "#B3261E"
typography:
  headline-display:
    fontFamily: "[Fuente de títulos]"
    fontSize: 48px
    fontWeight: 600
    lineHeight: 1.1
  headline-lg:
    fontFamily: "[Fuente de títulos]"
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.2
  headline-md:
    fontFamily: "[Fuente de títulos]"
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.25
  body-md:
    fontFamily: "[Fuente de textos]"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  label-md:
    fontFamily: "[Fuente de textos]"
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1
rounded:
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
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    padding: 12px 24px
  button-primary-hover:
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
  card-product:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-secondary}"
    rounded: "{rounded.md}"
    padding: "{spacing.md}"
  tag-offer:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.on-tertiary}"
    rounded: "{rounded.full}"
  input-field:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    padding: 12px 14px
  message-error:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.error}"
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface}"
  text-secondary:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.on-surface-variant}"
---

# [Nombre del emprendimiento] — Design system

## Overview

<!-- Qué es la marca, para quién es (tu proto-persona) y qué sensación
debe transmitir la interfaz (tus palabras clave del moodboard). -->

## Colors

<!-- Para qué se usa cada color y dónde NO se usa. Ejemplo:
- **Primary (#1F4E79):** botones principales, enlaces y logo. -->

## Typography

<!-- Qué familia va en títulos y cuál en textos, y la escala. -->

## Layout

<!-- Ancho máximo, márgenes, escala de espaciado, breakpoints
(mobile hasta 767px, tablet de 768 a 1023px, desktop desde 1024px)
y qué cambia en cada uno: columnas, menú, filtros, imágenes. -->

## Elevation & Depth

<!-- Cómo se marca la jerarquía: sombras, bordes o capas de color. -->

## Shapes

<!-- Radios de botones, tarjetas e inputs. -->

## Components

<!-- Un ### por componente: qué contiene, sus reglas concretas y sus
estados. Usa los mismos nombres de los tokens (card-product, button-primary). -->

## Do's and Don'ts

<!-- Lo que siempre y lo que nunca se hace. -->
