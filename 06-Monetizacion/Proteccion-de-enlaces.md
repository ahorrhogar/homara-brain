---
tags: [monetizacion, proteccion, afiliacion]
type: guia
estado: vigente
prio: alta
---

# Protección de enlaces afiliados

## Por qué
- Evitar scraping y robo de comisiones.
- Centralizar tracking.
- Permitir cambios de afiliado sin tocar contenido publicado.
- Cumplir directrices SEO (`rel="sponsored nofollow"`, redirección controlada).

## Patrón
- Todos los enlaces afiliados pasan por una **URL interna** (`/go/...` o similar) que:
  1. Loggea el click.
  2. Aplica el tag de afiliado actual.
  3. Redirige al partner.

## Reglas duras
- **Nunca** poner enlaces afiliados crudos en contenido.
- Cambios masivos: con backup + dry-run.
- Monitor de enlaces caídos (ver [[../05-Producto/Analitica-y-tracking]]).

## Volver
- [[_MOC-Monetizacion]]
