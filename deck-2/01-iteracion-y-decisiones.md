# Iteración y decisiones de diseño

Este es el documento que amarra el relato. Sirve para dos cosas a la vez: la lámina de iteración que pide el punto 3 del entregable, y la evidencia del **componente 5 del visado ABET**, que hoy está sin marcar.

El componente 5 exige: *"propuesta → testeo o verificación → modificación documentada y justificada por los resultados de la prueba"*. La entrevista es el testeo. Esto es la modificación.

---

## 1. La línea de tiempo

| Momento | Qué pasó | Qué decía el producto |
|---|---|---|
| **Septiembre 2026** | Deck 1, Módulo 1 | B2B núcleo (inmobiliarias), municipios, B2C como expansión futura. Prefiltro + membrana + electrostática. Dashboard y datos |
| **Octubre 2026** | Prácticas 2.1 y 2.4, Excel de costeo | Deriva a **B2C**: equipo bajo el lavamanos, venta a hogares a US$320, estimación con IA |
| **26 de octubre** | **Entrevista con el supervisor técnico** | "B2C es muy difícil. Es mejor enfocarse en B2B y B2G". "El sistema de filtros tiene que ser más sencillo". "No es necesario un sistema de monitoreo tan refinado con IA" |
| **29 de octubre** | Visado ABET, Revisión 1 | 6 de 8 componentes logrados. Iteración y solución final quedan pendientes |
| **Ahora** | Corrección | Vuelve a B2B colectivo, con respaldo normativo y de costos |

**El punto clave del relato:** no fue un giro improvisado. El Módulo 1 ya planteaba B2B. La deriva al B2C ocurrió mientras diseñaban el prototipo, y tres análisis independientes la corrigieron.

---

## 2. Las tres fuentes que apuntan al mismo lugar

Esto es lo que hace fuerte la lámina: no es la opinión de una persona.

| Fuente | Qué dice | Evidencia |
|---|---|---|
| **El supervisor técnico** | El B2C no funciona por el costo de conectar cañerías en vivienda existente | [Entrevista 26/10/2026](../modulo-2/2.3-entrevista-con-expertos.md) |
| **El DS 40** | Un equipo por departamento con UV obliga a un análisis de laboratorio mensual: CLP 65.787 por depto, US$790 al año. Compartido en un edificio, baja a US$1,3 por depto al mes | [Artículos 43, 44 y 45](03-normativa-y-requisitos.md) |
| **El cálculo de ahorro** | Una vivienda ahorra US$6,4 al mes y se le cobraba US$8 de mantención: **el cliente perdía US$19 al año** | [Tarifa ESSBIO real](04-ahorro-precio-y-unidad-economica.md) |

Tres caminos distintos (comercial, regulatorio y económico) que llegan a la misma conclusión: **el producto es una planta colectiva de edificio, vendida a la inmobiliaria en obra nueva.**

---

## 3. Qué cambia, decisión por decisión

| # | Decisión | Antes | Ahora | Por qué |
|---|---|---|---|---|
| 1 | **Arquitectura** | Equipo compacto bajo el lavamanos, uno por departamento | **Planta colectiva por edificio** | El costo de cumplimiento del DS 40 se divide entre todos los departamentos en vez de repetirse |
| 2 | **Cliente primario** | Hogares (B2C) | **Inmobiliarias y constructoras en obra nueva** (B2B), municipios (B2G) | Entrevista: el costo de instalación mata el B2C. En obra nueva la doble tubería entra en planos |
| 3 | **Quién paga qué** | Un solo cliente paga todo | **La inmobiliaria compra el equipo; la comunidad paga la suscripción** | A la inmobiliaria no le importa el payback. A la comunidad sí, y su suscripción es menor que su ahorro |
| 4 | **Tren de tratamiento** | Prefiltro + membrana + separación electrostática | **Prefiltro + microfiltración con carbón + desinfección** | Entrevista: "tiene que ser más sencillo, debido al uso que tenemos pensado del agua". La electrostática ya había salido del Excel |
| 5 | **Monitoreo** | IA predictiva, dashboard, nube | **Sensores en línea + registro automático + reporte de cumplimiento** | Entrevista: "no es necesario un sistema de monitoreo tan refinado con IA". Pero el DS 40 art. 44 **sí exige registro y seguimiento**, así que la capa de datos se mantiene con otra justificación |
| 6 | **Propuesta de valor** | "Agua tratada con datos accionables" | **"Agua reutilizable más el expediente que prueba que cumple"** | Ningún competidor chileno se posiciona sobre el cumplimiento automatizado |
| 7 | **Precio** | US$320 el equipo + US$8 al mes de mantención, que costaba más que el ahorro | **~US$560 por vivienda** en planta colectiva, más US$150 al mes por edificio (US$3 por vivienda) | El cliente pasa de perder US$19 al año a ganar US$40. Ver [04](04-ahorro-precio-y-unidad-economica.md) |
| 8 | **Argumento normativo** | "La normativa exige reutilizar" | **"La normativa no obliga todavía, pero regula con detalle a quien reutiliza, y la OGUC puede hacerlo obligatorio"** | La Ley 21.075 es permisiva. Su art. 14 delega la obligatoriedad en la OGUC |

---

## 4. Lo que NO cambia

Vale la pena decirlo en la lámina, porque demuestra que la iteración fue quirúrgica y no un borrón y cuenta nueva:

- **El problema** y su dimensionamiento siguen siendo los mismos.
- **El presupuesto de los meses 1 a 9** del prototipo beta se mantiene. Siguen construyendo un prototipo para probar el tren de tratamiento y la capa de sensores. Que el prototipo sea una unidad de banco está bien: es un prototipo, no el producto.
- **La capa de datos** sigue siendo el diferenciador, solo que ahora se justifica con el artículo 44 del DS 40 en vez de con "IA predictiva".
- **El foco en obra nueva** ya estaba en el deck 1.

---

## 5. Cómo contarlo en la presentación

Una sola lámina, tres bloques:

**Planteamos** → Equipo por departamento, venta directa al hogar, monitoreo con IA.

**Probamos** → Entrevista con un académico de Ingeniería Industrial UdeC (26/10/2026) sobre tres desafíos. Más revisión del DS 40 y cálculo de ahorro con tarifa ESSBIO real.

**Cambiamos** → Planta colectiva, venta a inmobiliaria en obra nueva, suscripción de cumplimiento a la comunidad. Con los dos números que lo prueban: el costo de cumplimiento por vivienda baja de **US$792 a US$16 al año**, y el cliente pasa de **perder US$19 al año a ganar US$40**.

Esos dos números son los que hay que dejar en la lámina. Son concretos, vienen de la norma, de la tarifa real y del propio Excel del grupo, y explican la decisión mejor que cualquier párrafo.

---

## 6. Para el visado ABET

Con esto, el **componente 5** pasa de sin marcar a defendible:

| Lo que exige la rúbrica | Dónde está |
|---|---|
| Propuesta | Prototipo alfa (práctica 1.2) y diseño beta (práctica 2.1) |
| Testeo o verificación | Entrevista con supervisor técnico (práctica 2.3), análisis del DS 40, cálculo de ahorro |
| Modificación documentada y justificada | Este documento, sección 3 |

Y el **componente 8** (calidad de la solución final) pide *"resultados esperados cuantificados y comparados contra la línea base"*. La línea base es la cuenta de agua actual; el resultado esperado es el ahorro de US$3.819 al año por edificio. Eso ya está calculado en [04](04-ahorro-precio-y-unidad-economica.md).
