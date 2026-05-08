---
tags: [sistema, convenciones]
type: guia
---

# Convenciones de naming

## Carpetas

- Prefijo numérico de dos dígitos: `01-Empresa`, `02-Estrategia`, …
- Prefijo `_` para utilitarias: `_Plantillas`, `_Adjuntos`, `_Diario`.

## Ficheros

- `Kebab-Title-Case` en español **sin acentos** ni `ñ` para máxima compatibilidad: `Modelo-de-negocio.md`, `Identidad-de-marca.md`.
- Si la nota es un MOC: prefijo `_MOC-` → `_MOC-SEO.md`.
- Plantillas con prefijo `Plantilla-` → `Plantilla-Articulo.md`.

## Aliases

- Usa `aliases:` en frontmatter para añadir variantes con acentos o nombres alternativos:

```yaml
aliases: [Modelo de Negocio, Business Model]
```

## Volver
- [[_MOC-Sistema]]
