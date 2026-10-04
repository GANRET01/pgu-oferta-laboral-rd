# Pensiones no contributivas y oferta laboral: evidencia de regresión discontinua para la PGU en Chile

Estudio del efecto de la Pensión Garantizada Universal (PGU, 2022) sobre la participación laboral y las horas trabajadas en Chile, usando un diseño de regresión discontinua (RD) alrededor del umbral de elegibilidad de 65 años, con datos de la Encuesta CASEN 2017 y 2022.

📄 **Columna corta (VoxEU-style):** [`columna_voxeu_pgu.md`](./columna_voxeu_pgu.md)
📘 **Informe extenso:** [`informe_extenso_PGU.Rmd`](./informe_extenso_PGU.Rmd) — contiene el marco teórico completo, la estrategia de identificación, todos los resultados y el ejercicio de robustez. Este README es solo un resumen de orientación.

## El proyecto en breve

La PGU reemplazó al sistema solidario anterior (PBS-APS), expandiendo la cobertura del 60% al 90% de los hogares, manteniendo el umbral de 65 años. Esto permite dos estrategias de identificación:

1. **RD agudo/difuso alrededor de los 65 años** (2017 y 2022, por separado), para estimar:
   - **Opción A** — efecto directo sobre el beneficiario elegible.
   - **Opción B** — derrame sobre otros integrantes del hogar en edad de trabajar, siguiendo a Bertrand, Miller & Mullainathan (2003).
2. **RD-DiD (diferencias-en-discontinuidades)** — para el percentil 60-90 de ingreso, que la reforma incorporó por primera vez a la cobertura solidaria, se compara el salto de comportamiento laboral en 2022 contra el mismo salto en 2017 (cuando ese tramo no calificaba a ningún beneficio). Esto aísla el efecto específico de la reforma del efecto más general de cumplir 65 años en Chile.

## Supuestos clave

- La edad no es manipulable por los individuos para calificar al beneficio (supuesto de identificación estándar en RD).
- Se documenta y declara evidencia de *heaping* (redondeo) de edad en los datos — no manipulación estratégica — que motiva un ejercicio de robustez más exigente de lo habitual (*donut RD*, sensibilidad a bandwidth, aleatorización local).
- Se declara explícitamente, con evidencia propia (falla de una prueba placebo), que el umbral de 65 años en Chile no captura exclusivamente el efecto de la PGU, sino que coincide con otros cambios asociados a la edad de jubilación en un sentido más amplio.

## Hallazgos principales

- **No hay evidencia robusta de que la PGU reduzca la probabilidad de estar ocupado** en el tramo de ingreso donde la reforma expandió la cobertura (percentil 60-90).
- **Sí hay evidencia sólida de una reducción de ~6.6 horas semanales trabajadas** entre quienes permanecen empleados en ese mismo tramo — el hallazgo más creíble del estudio, robusto a múltiples chequeos (*donut RD*, bandwidths alternativos, tanto a nivel de cada año como en la comparación formal 2022 vs. 2017).
- El efecto directo estimado sobre la muestra completa (sin restringir por ingreso) es mayor en magnitud, pero de robustez desigual — se reporta con las cautelas correspondientes.
- El derrame intrahogar (Opción B) es, en el mejor de los casos, sugestivo; no se replica el canal de género documentado por Bertrand et al. (2003).

## Estructura del repositorio

```
├── RD-PGUgit.Rmd                 # Pipeline completo de análisis (carga, construcción de
│                                # variables, Opción A, Opción B, RD-DiD, robustez, figuras)
├── informe_extenso_PGU.Rmd      # Informe completo (marco teórico, resultados, discusión)
├── columna_voxeu_pgu.md         # Columna corta de divulgación
├── bitacora_decisiones_y_resultados.md  # Registro de decisiones metodológicas y resultados
└── Data/                         # No incluida (ver más abajo)
```

## Cómo reproducir el análisis

1. Descarga las bases CASEN 2017 y 2022 (formato `.RData`) desde los links en la sección "Referencias" y colócalas en una carpeta `Data/` local (no incluida en este repositorio).
2. Ajusta las rutas de carga al inicio de RD-PGUgit.Rmd`.
3. Abre el archivo en RStudio y usa **"Run All"** de principio a fin en una sola pasada (el pipeline tiene dependencias secuenciales entre secciones).
4. Para el informe en HTML, usa "Knit" sobre `informe_extenso_PGU.Rmd`.

**Nota sobre los datos:** las bases CASEN no se redistribuyen en este repositorio por su tamaño y para respetar los términos de uso de la encuesta. Solo se incluyen el código y los resultados derivados.

## Nota de transparencia sobre uso de IA

El código de este repositorio fue desarrollado de forma iterativa con asistencia de Claude (Anthropic), incluyendo depuración y estructuración. El informe extenso y la columna de divulgación fueron redactados con asistencia mínima del mismo modelo a partir de los resultados del análisis. Todas las decisiones de diseño metodológico, la validación de variables contra el libro de códigos de CASEN, y la interpretación de resultados fueron realizadas y verificadas por el autor.

## Referencias principales

- Bertrand, M., Miller, D., & Mullainathan, S. (2003). Public Policy and Extended Families: Evidence from Pensions in South Africa. *The World Bank Economic Review*, 17(1), 27–50.
- Cattaneo, M. D., Idrobo, N., & Titiunik, R. (2019–2024). *A Practical Introduction to Regression Discontinuity Designs*. Cambridge University Press.
- Vergara Bustos, I. (2025). Impacto de la Pensión Garantizada Universal en la participación laboral y formalidad del empleo. *Estudios Públicos*.

# Datos
Casen 2017
https://bidat.gob.cl/details/ficha/dataset/bases-de-datos-casen-2017

Casen 2022
https://bidat.gob.cl/details/ficha/dataset/base-de-datos-casen-2022

---

**Autor:** Gonzalo Reyes 
