---
tags: [seo, tecnico]
type: guia
estado: borrador
---

# SEO técnico

## Imprescindibles
- **Sitemap dinámico** ✅ (ya implementado).
- **Robots.txt** revisado y consistente.
- **Canonicals** correctos en filtros y paginaciones.
- **Schema.org**:
  - `Product` + `Offer` en fichas.
  - `Article` + `BreadcrumbList` en blog.
  - `ItemList` en rankings.
  - `FAQPage` cuando aplique.
- **Open Graph / Twitter Card** en todo.
- **hreflang** preparado para [[../09-Crecimiento/Expansion-internacional|expansión internacional]].

## Rendimiento (Core Web Vitals)
- LCP < 2.5s.
- CLS < 0.1.
- INP < 200ms.
- Imágenes en formatos modernos (AVIF/WebP) + lazy load.

## Crawl
- URLs de filtros: noindex o canonical apuntando al padre, salvo intención propia.
- Paginación con `rel=next/prev` opcional + canonical.
- Search internal: noindex.

## Pendiente
- Auditoría inicial documentada.
- Plan de monitoreo (Search Console + log analysis).

## Volver
- [[_MOC-SEO]] · [[../05-Producto/Arquitectura]]
