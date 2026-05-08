---
tags: [sistema, indice]
type: indice
---

# Índice general

> Tip: si tienes Dataview instalado, sustituye estos enlaces por una query.

## Por área

- 🏢 [[../01-Empresa/_MOC-Empresa|Empresa]]
- 🎯 [[../02-Estrategia/_MOC-Estrategia|Estrategia]]
- 🔎 [[../03-SEO/_MOC-SEO|SEO]]
- ✍️ [[../04-Contenido/_MOC-Contenido|Contenido]]
- 💻 [[../05-Producto/_MOC-Producto|Producto]]
- 💸 [[../06-Monetizacion/_MOC-Monetizacion|Monetización]]
- 🛒 [[../07-Categorias/_MOC-Categorias|Categorías]]
- ⚙️ [[../08-Operaciones/_MOC-Operaciones|Operaciones]]
- 🚀 [[../09-Crecimiento/_MOC-Crecimiento|Crecimiento]]
- 🌍 [[../10-Mercado/_MOC-Mercado|Mercado]]

## Query Dataview (opcional)

```dataview
TABLE file.folder AS "Carpeta", file.mtime AS "Modificada"
FROM ""
WHERE !contains(file.path, "_Plantillas") AND !contains(file.path, "_Adjuntos")
SORT file.mtime DESC
LIMIT 30
```

## Volver
- [[_MOC-Sistema]] · [[../Inicio|Inicio]]
