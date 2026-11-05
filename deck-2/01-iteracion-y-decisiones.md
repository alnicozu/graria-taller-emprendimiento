# Iteración y decisiones de diseño

Este documento amarra el relato. Sirve para la lámina de iteración del deck y como evidencia del **componente 5 del visado ABET**, que exige *"propuesta → testeo o verificación → modificación documentada y justificada"*.

---

## 1. La línea de tiempo

| Momento | Qué pasó | Qué decía el producto |
|---|---|---|
| **Septiembre 2026** | Deck 1, Módulo 1 | Equipo compacto bajo el vanitorio, uno por baño, a US$3.000 por vivienda. Prefiltro, membrana y electrostática. Reúso solo en WC |
| **Evaluación 1** | Retroalimentación del profesor | **"Baño por baño va a salir muy caro"**. Tenía razón: a ese precio el payback era de 31 años |
| **Octubre 2026** | Prácticas 2.1 y 2.4, Excel de costeo | Deriva a venta directa al hogar (B2C) a US$320, con estimación por IA |
| **26 de octubre** | **Entrevista con el supervisor técnico** | "B2C es muy difícil por el costo de instalación. Mejor B2B y B2G". "El sistema de filtros tiene que ser más sencillo". "No hace falta IA" |
| **29 de octubre** | Visado ABET, Revisión 1 | 6 de 8 componentes logrados. Iteración y solución final pendientes |
| **Noviembre** | Revisión del DS 40 y de la tarifa vigente | El art. 43 hace inviable la UV en equipos individuales. La tarifa real es 26% mayor que la de 2022 |
| **Ahora** | Corrección | **Casas en obra nueva, vendidas por lote a constructoras, con cloración y reúso en WC más riego** |

---

## 2. Las cuatro fuentes que ordenaron el diseño

Lo que hace fuerte la lámina es que no es la opinión de una persona.

| Fuente | Qué dijo | Qué cambió |
|---|---|---|
| **El profesor** (Evaluación 1) | Baño por baño sale muy caro | Obligó a bajar el costo de verdad, no a maquillarlo |
| **El supervisor técnico** (26/10) | B2C no funciona; B2B y B2G sí | El cliente es la constructora, no el hogar |
| **El DS 40** (arts. 8, 43 y 45) | Con UV, laboratorio mensual por sistema: US$789 al año por casa | Cloración en vez de UV |
| **La tarifa ESSBIO** (23-09-2026) | 1.576 $/m³ sumando agua y alcantarillado | El ahorro real es mayor de lo que creíamos |

---

## 3. Qué cambia, decisión por decisión

| # | Decisión | Antes | Ahora | Por qué |
|---|---|---|---|---|
| 1 | **Dónde se instala** | Bajo el vanitorio, miniaturizado | **En la logia o el patio de la casa** | Hay espacio: no necesita chasis a medida. Baja ~US$20 del costo |
| 2 | **Cliente** | Hogar directo (B2C) | **Constructora en obra nueva**, que compra el proyecto completo | Entrevista: el costo de instalación mata el B2C |
| 3 | **Para qué se reutiliza** | Solo descarga de WC | **WC más riego de jardín** | La casa riega. Pasa de 5,10 a 8,85 m³/mes y el ahorro de US$96 a US$167 |
| 4 | **Desinfección** | UV | **Cloración** | DS 40: con UV el art. 43 exige laboratorio mensual (US$789/año por casa); con cloro el art. 45 pide medición semanal portátil |
| 5 | **Tren de tratamiento** | Prefiltro, membrana y electrostática | **Prefiltro, microfiltración con carbón y cloración** | Entrevista: "tiene que ser más sencillo". La electrostática además pedía 3.000 a 9.000 V |
| 6 | **Monitoreo** | IA predictiva y dashboard | **Sensor de cloro en línea y registro automático** | La IA no hacía falta, pero el art. 45 **sí exige** registro ordenado semanal |
| 7 | **Precio** | US$3.000 por vivienda | **US$480 por casa instalada**, más US$4 al mes | Payback de 31 a 2,9 años. Esa era la objeción |
| 8 | **Argumento normativo** | "La normativa exige reutilizar" | **"No obliga todavía, pero regula con detalle a quien lo hace"** | La Ley 21.075 es permisiva; su art. 14 delega la obligatoriedad en la OGUC |

---

## 4. Lo que NO cambia

- **El problema** y su marco siguen siendo los mismos.
- **El presupuesto de los meses 1 a 9** se mantiene: siguen construyendo un prototipo. Única salvedad: la línea del esterilizador UV hay que reemplazarla por el dosificador y el sensor de cloro, pendiente de cotizar.
- **La capa de datos** sigue siendo el diferenciador, ahora justificada por el art. 45 en vez de por "IA predictiva".
- **El foco en obra nueva** ya estaba en el deck 1.

---

## 5. Cómo contarlo en la presentación

**Nos dijeron** → que baño por baño saldría muy caro. A US$3.000 por vivienda, el payback era de 31 años.

**Fuimos a probar** → entrevista con un académico de Ingeniería Industrial, lectura completa del DS 40 y búsqueda de la tarifa vigente de ESSBIO.

**Cambiamos dos cosas** → la casa riega, así que reutiliza casi el doble que un departamento. Y el reglamento nos dijo que con UV el cumplimiento costaba US$789 al año por casa, así que pasamos a cloración.

**El resultado** → de **31 años a 2,9 años** de recuperación. No bajamos el precio a la fuerza: encontramos dónde estaba el valor.

---

## 6. Para el visado ABET

| Lo que exige la rúbrica | Dónde está |
|---|---|
| Propuesta | Prototipo alfa (práctica 1.2) y diseño beta (práctica 2.1) |
| Testeo o verificación | Retroalimentación de la Evaluación 1, entrevista con supervisor (práctica 2.3), análisis del DS 40, cálculo con tarifa real |
| Modificación documentada y justificada | Este documento, sección 3 |

El **componente 8** pide *"resultados esperados cuantificados y comparados contra la línea base"*. La línea base es la cuenta de agua actual; el resultado esperado es el ahorro de US$167 al año por casa. El cálculo está en [09-como-se-calculo-todo.md](09-como-se-calculo-todo.md).
