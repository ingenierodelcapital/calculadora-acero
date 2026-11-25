# Calculadora de acero corrugado

Herramienta web para medir los **kg de armadura (B500S)** de estructuras de hormigón armado y preparar la certificación.

## Qué hace
- **Mallas** (muros, losas, soleras, zapatas): longitud × altura, 1 o 2 caras, diámetro y separación en cada sentido, patillas.
- **Barras sueltas**: esperas, refuerzos, cercos (nº de barras × longitud).
- **Solapes** cuando una barra supera la longitud comercial (12 m por defecto), por dos métodos:
  - nº de diámetros (ls = n·Ø), expresado en mm o cm;
  - tabla EHE-08 (art. 69.5, método simplificado) con posición I / II, hormigón, acero y coeficiente α. Tablas editables.
- **Pesos por diámetro** consultables y editables.
- **Informe de justificación** (criterios, planilla de despiece, resúmenes, firmas) listo para imprimir o guardar en PDF.
- Resumen por diámetros, total en kg y cuantía en kg/m².
- Exporta a **Excel (CSV)** y guarda o abre proyectos (.json).

## Fórmulas
- Peso lineal: `kg/m = π·Ø²/4 · 7850 / 10⁶` (Ø12 = 0,888 · Ø16 = 1,578)
- Nº de barras: `redondeo arriba(ancho / separación) + 1`
- Solapes: `redondeo arriba((L − Lc) / (Lc − Lsolape))`

## Uso
Abre `index.html` en cualquier navegador, también desde el móvil. No necesita instalación ni internet.
