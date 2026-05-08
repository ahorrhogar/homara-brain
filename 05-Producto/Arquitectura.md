---
tags: [producto, arquitectura]
type: guia
estado: vigente
---

# Arquitectura

Visión de alto nivel del sistema actual.

## Componentes

- **Frontend** público (web visible al usuario).
- **Panel de administración** (gestión editorial y de productos).
- **Supabase** como base de datos y backend de servicios.
- **Sistema de artículos SEO** (categorías, subcategorías, productos, ofertas).
- **Analítica interna** + tracking de clicks.
- **Protección de enlaces afiliados**.
- **Sistema de cookies**.
- **Sitemap dinámico**.

## Diagrama mental

`Usuario → Frontend → API/Supabase → Render contenido (artículo / categoría / ficha) → Click afiliado (protegido + tracked) → Partner`

## Por documentar
- Diagramas (subir a `_Adjuntos/`).
- Endpoints internos clave.
- Procesos batch (sitemap, refresco de ofertas).

## Relacionado
- [[Stack-tecnico]] · [[Base-de-datos-Supabase]] · [[Panel-admin]]

## Volver
- [[_MOC-Producto]]
