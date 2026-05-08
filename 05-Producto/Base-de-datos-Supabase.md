---
tags: [producto, supabase, db]
type: guia
estado: borrador
---

# Base de datos · Supabase

> Documenta aquí entidades, relaciones y reglas. Si crece, divide por entidad.

## Entidades probables

- `categorias` (jerárquicas)
- `subcategorias`
- `productos`
- `ofertas` (precio, partner, vigencia, histórico)
- `articulos` (tipo, categoría, slug, status)
- `clicks` (tracking afiliado)
- `usuarios_admin`

## Reglas
- **No tocar afiliados ni URLs de productos** sin justificación documentada.
- Cualquier migración con backup previo.
- Esquemas con `created_at` / `updated_at` siempre.

## Pendiente
- Diagrama ER en `_Adjuntos/`.
- Backups automatizados documentados.
- Políticas RLS revisadas.

## Volver
- [[_MOC-Producto]]
