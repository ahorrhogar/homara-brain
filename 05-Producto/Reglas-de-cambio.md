---
tags: [producto, reglas]
type: guia
estado: vigente
prio: alta
---

# Reglas de cambio

> Las reglas que protegen la base técnica. Antes de tocar algo, leer.

1. **No romper UI/UX existente.** Cambios visuales con justificación y, si afectan a producción, con preview.
2. **No tocar lógica de negocio** si no es estrictamente necesario.
3. **No cambiar afiliados ni URLs de productos** existentes (perder histórico = perder ingresos).
4. **No modificar arquitectura sin justificación documentada** (crear nota con [[../_Plantillas/Plantilla-Decision]]).
5. **Priorizar siempre estabilidad, SEO y conversión.**
6. **Si algo puede hacerse de forma más segura, elegir la opción segura.**
7. **Todo cambio debe ser escalable y reversible.**
8. Cambios sensibles → backup + plan de rollback.

## Volver
- [[_MOC-Producto]]
