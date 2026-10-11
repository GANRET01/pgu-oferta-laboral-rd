

# La PGU no expulsó a los chilenos del mercado laboral, aunque sí recortó sus jornadas

*Resultados de un diseño de regresión discontinua aplicado a las encuestas CASEN de 2017 y 2022*

---

En febrero de 2022, Chile dejó atrás su esquema de pensiones solidarias —dividido entre la Pensión Básica Solidaria y el Aporte Previsional Solidario, y acotado al 60% de los hogares de menores ingresos— para dar paso a la Pensión Garantizada Universal (PGU), un aporte no contributivo que en la actualidad alcanza al 90% de las personas mayores de 65 años. Hay una interrogante que pocas evaluaciones de este tipo de reformas consiguen contestar con solidez, y que resulta tan sencilla como incómoda: **si el Estado asegura un ingreso en la vejez, ¿la gente deja de trabajar?**

A partir de la Encuesta CASEN de 2017 y 2022, y valiéndonos de un diseño de regresión discontinua (RD) en torno al umbral etario de los 65 años, la respuesta que hallamos es matizada: **en términos generales, la PGU no provocó que las personas abandonaran el mercado laboral, pero aquellos que continúan trabajando recortaron sus horas de manera considerable**, y ese efecto puede aislarse con limpieza en el grupo poblacional donde la reforma efectivamente modificó las reglas del juego.

## El cuasi-experimento que surgió sin proponérselo

La estrategia explota dos fuentes de variación que se superponen. Por un lado está el umbral de edad: dado que nadie puede alterar su fecha de nacimiento para acceder al beneficio, contrastar a quienes están a punto de cumplir 65 años con quienes acaban de cumplirlos se asemeja bastante a un experimento aleatorizado. Por otro lado, la PGU **amplió la cobertura** en comparación con el sistema que le precedía: los hogares ubicados entre los percentiles 60 y 90 de ingreso, un sector de la población que antes de 2022 no accedía a ningún beneficio solidario al llegar a los 65, ahora sí califican.

Esto habilita una comparación adicional: si el salto en el comportamiento laboral a los 65 años se manifiesta en 2022 pero no en 2017 **dentro de ese mismo segmento de ingreso**, entonces la explicación más razonable deja de ser "las personas modifican su conducta al cumplir 65 años" en términos generales (jubilación social, pautas culturales, otros beneficios para adultos mayores) y pasa a ser, específicamente, la PGU.

**Este segundo diseño —una diferencia-en-discontinuidades— constituye la evidencia más creíble del estudio**, justamente porque no se apoya en el supuesto, más endeble, de que ninguna otra cosa cambia exactamente a los 65 años.

## Primer resultado: los incentivos sí se modificaron con la reforma

Antes de examinar los efectos, corresponde verificar que el "tratamiento" ocurrió de verdad. La Figura 1 presenta la probabilidad de recibir el beneficio solidario según la edad, centrada en el corte: esta asciende desde prácticamente cero hasta cerca del 50% justo a los 65 años.
<img width="329" height="203" alt="motivador" src="https://github.com/user-attachments/assets/bde78dbf-80ed-4726-8900-132784a234b0" />

*Figura 1. Probabilidad de recibir la PGU, CASEN 2022. El salto discreto en el umbral constituye la base de la identificación: confirma que cruzar los 65 años altera sustancialmente el acceso al beneficio, lo que permite aislar su efecto sobre el comportamiento laboral.*

## El hallazgo central: el ajuste ocurre en las horas, no en la decisión de trabajar

En el segmento de ingreso donde la reforma realmente amplió la cobertura (percentiles 60-90), el contraste entre ambos años resulta nítido:
<img width="360" height="172" alt="000012" src="https://github.com/user-attachments/assets/7185e580-9ad0-4ff3-b6dc-6d3578e99da4" />


*Figura 2. Efecto de cruzar los 65 años sobre las horas semanales trabajadas, percentil 60-90 de ingreso. En 2017 —cuando este tramo de ingreso no calificaba al sistema solidario— no se observa reducción alguna; de hecho, el punto estimado es positivo. En 2022 —cuando sí calificó gracias a la PGU— el efecto equivale a una caída de 4.5 horas semanales, con intervalos de confianza que no se solapan entre ambos años.*

La brecha entre ambos años —lo que técnicamente se denomina efecto diferencia-en-discontinuidades— asciende a **6.6 horas semanales menos**, con alta significancia (p<0.001) y robusta a la exclusión de observaciones muy próximas al corte de edad (un chequeo estándar en esta literatura, conocido como "donut RD"), tanto al estimar 2022 por sí solo como en la comparación formal contra 2017. En cambio, no hallamos evidencia robusta de que la reforma haya alterado la *probabilidad* de continuar trabajando dentro de ese mismo tramo de ingreso: el efecto se concentra íntegramente en el margen intensivo.

Este patrón resulta económicamente consistente: es precisamente lo que cabe esperar de un efecto ingreso puro, sin restricciones de liquidez que obliguen a una salida total del mercado laboral. Las personas no necesitan dejar de trabajar por completo, de modo que ajustan por el margen que les resulta menos costoso, disminuyendo su carga horaria en lugar de renunciar.

## ¿Qué ocurre con el efecto sobre la población completa, más allá de este tramo de ingreso?

Si observamos al conjunto de los beneficiarios (no únicamente al tramo de ingreso recién descrito), el patrón es de mayor magnitud pero también más frágil: una caída de 15 a 17 puntos porcentuales en la probabilidad de encontrarse ocupado, y de aproximadamente 10 horas semanales entre quienes continúan trabajando. No obstante, a diferencia del resultado del diseño diferencia-en-discontinuidades, esta estimación no permite descartar que esté recogiendo, en parte, conductas vinculadas a cumplir 65 años en general —y no a la PGU en particular—. Confirmamos esta limitación mediante una prueba adicional: características del hogar que en teoría no deberían alterarse por un cambio de ingreso en el corto plazo, como la tenencia de la vivienda, también registran un salto en el umbral de los 65 años, en ambos años de la muestra. Esto apunta a que cumplir 65 años en Chile viene acompañado de modificaciones reales en la convivencia y en los arreglos familiares, con independencia de cualquier política de pensiones — una razón más para privilegiar el resultado del diseño diferencia-en-discontinuidades por sobre el efecto "crudo" en el umbral etario.

## Implicancias para la política pública

Tres consecuencias, con distintos grados de certeza:

**Con alta confianza:** la PGU no está vaciando de forma generalizada el mercado laboral de los adultos mayores. El margen de ajuste es la intensidad, no la participación.

**Con confianza moderada:** para la clase media que la reforma incorporó por primera vez a un beneficio solidario, el costo fiscal de la PGU viene acompañado de una reducción medible en la oferta laboral de quienes permanecen empleados — información pertinente para proyectar el impacto fiscal de segunda ronda de la reforma (menor recaudación, menores cotizaciones) y para el diseño de eventuales ajustes futuros al beneficio.

**Como advertencia metodológica para el resto de esta literatura:** una parte importante de los estudios sobre pensiones y oferta laboral que emplean el corte de edad como fuente de variación —tanto en Chile como en otros países— corre el riesgo de confundir el efecto del beneficio con el efecto de alcanzar la edad de jubilación en un sentido más amplio. El diseño diferencia-en-discontinuidades aquí utilizado brinda una manera de separar ambos efectos cuando existe variación en la cobertura del beneficio a lo largo del tiempo, y debería adoptarse como estándar siempre que dicha variación esté disponible.

---

### Referencias

Bertrand, M., Miller, D., & Mullainathan, S. (2003). "Public Policy and Extended Families: Evidence from Pensions in South Africa." *The World Bank Economic Review*, 17(1), 27-50.

Cattaneo, M. D., Idrobo, N., & Titiunik, R. (2019-2024). *A Practical Introduction to Regression Discontinuity Designs*. Cambridge University Press.

Vergara Bustos, [inicial] (2025). "Impacto de la Pensión Garantizada Universal en la participación laboral y formalidad del empleo." *Estudios Públicos*.

---

*Nota metodológica: las estimaciones emplean `rdrobust` (Calonico, Cattaneo & Titiunik) con inferencia robusta corregida por sesgo y errores estándar agrupados por edad entera, dada la naturaleza discreta de la variable de edad en la encuesta. El código y los detalles completos de la construcción de variables están disponibles en el repositorio del proyecto.*
