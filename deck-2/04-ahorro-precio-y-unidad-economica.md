# Ahorro, precio y unidad económica

El supervisor técnico lo pidió explícitamente: *"es importante determinar el gasto en agua y cuánto se ahorrarían los consumidores con este sistema de filtrado, debido a que puede ser determinante para el cambio de tecnología"*.

Ese cálculo no existía en ninguna parte del block. Acá está, con tarifa real, y el resultado cambia el modelo de negocio.

---

## 1. La tarifa que corresponde a Concepción

Fuente: aviso oficial de tarifas de **ESSBIO S.A.**, regiones de Ñuble y Biobío. El propio aviso lista a **Concepción** dentro del **Grupo 1, Cuenca Bío Bío**, junto con Chiguayante, Penco, San Pedro, Talcahuano, Coronel, Lota y Tomé.

| Concepto | Valor |
|---|---|
| Cargo fijo por cliente | **$732 / mes** |
| Agua potable, período no punta (abril a noviembre) | **540,81 $/m³** |
| Alcantarillado, incluye tratamiento de aguas servidas | **707,21 $/m³** |
| **Total variable** | **1.248,02 $/m³** |
| Agua potable en sobreconsumo | 1.183,46 $/m³ |

Dos cosas importantes:

- **El alcantarillado se cobra sobre el agua potable medida**, no sobre la descarga real. Al comprar menos agua potable se ahorra en las dos líneas de la boleta. El ahorro es 1.248 $/m³, no los 541 $/m³ del agua potable sola.
- El aviso verificable es de **marzo de 2022**. Las tarifas subieron desde entonces (la SISS anunció alza gradual hasta 5% entre 2025 y 2030, más reajustes por IPC). **Usar 1.248 $/m³ es conservador.**

> **Tarea de 10 minutos:** que alguien fotografíe su boleta de ESSBIO y saque el $/m³ vigente. Citar una boleta de este mes en vez de un aviso de 2022 es el tipo de dato que el manual llama *"línea base con datos verificables"*.

---

## 2. Cuánto ahorra una vivienda

**Supuestos, todos de fuentes propias del grupo:**

| Supuesto | Valor | Fuente |
|---|---|---|
| Personas por hogar | 4 | Supuesto del equipo |
| Consumo por persona | 170 L/día | Deck 1, lámina 5 (Corporación Ciudades) |
| Consumo del hogar | 680 L/día = **20,4 m³/mes** | Cálculo |
| Participación del WC | **25%** | Resumen del Excel del grupo |
| Demanda de WC | **5,1 m³/mes** | Cálculo |
| Agua gris disponible | 9,6 a 14,4 m³/mes | Deck 1, lámina 7: ducha 80-120 L por uso |

El agua gris disponible es casi el triple de lo que consume el WC. **El límite no es cuánta agua gris hay, sino cuánta se puede reutilizar.** El sistema se dimensiona por la demanda del WC.

| Ahorro | Cálculo | Resultado |
|---|---|---|
| Mensual | 5,1 m³ × 1.248 $/m³ | **$6.365 ≈ US$6,4** |
| Anual | × 12 | **$76.380 ≈ US$76** |

**Por edificio de 50 departamentos:** 255 m³/mes, **US$3.819 al año**. Más el riego de áreas comunes, que no está contado.

---

## 3. El problema que revela el cálculo

Aquí está el hallazgo que ordena todo. Con el ahorro ya calculado, se puede contrastar contra el modelo del Excel:

| Concepto | Valor | Fuente |
|---|---|---|
| Ahorro del cliente | **US$6,4 / mes** | Cálculo con tarifa ESSBIO |
| Plan de mantención que se le cobra | **US$8,0 / mes** | Excel, supuesto 2 del plan de crecimiento |
| **Resultado para el cliente** | **−US$1,6 / mes** | |

**Un hogar con Graria pierde alrededor de US$19 al año**, antes de considerar los US$320 del equipo, que a ese ritmo no se recuperan nunca.

La suscripción cuesta más que el agua que ahorra. Eso explica, con números y sin opiniones, por qué el supervisor dijo que el B2C es muy difícil. Es la lámina más contundente que pueden mostrar.

> **Corrección a un análisis anterior:** el margen del equipo **no** era cero. El Excel estima el costo variable a volumen en **US$195** por equipo (electrónica US$55, filtración y UV US$60, hidráulica e instalación US$65, despacho US$15), lo que da **39% de margen bruto** sobre los US$320. El problema no era el margen del hardware, era la relación entre la suscripción y el ahorro.

---

## 4. El segundo problema: el costo de cumplimiento está subestimado

El Excel presupuesta el laboratorio así (supuesto 5): *"Laboratorio: control de calidad trimestral (USD 66)"*, y en la fila de gastos aparece una sola vez cada tres meses, para toda la operación.

Pero el **DS 40, artículo 43** exige que los sistemas con desinfección distinta a la cloración (es decir, UV) verifiquen la calidad bacteriológica **con frecuencia mensual**, y eso aplica **por sistema**, no por empresa.

La diferencia a escala es brutal:

| | Lo presupuestado | Lo que exige la norma |
|---|---|---|
| Frecuencia | Trimestral | **Mensual** |
| Alcance | Uno para toda la operación | **Uno por sistema instalado** |
| Costo al mes 48 (1.064 clientes activos) | US$22 al mes | **US$70.224 al mes** |

Al mes 48 el plan proyecta ingresos totales de **US$30.912 al mes**. El costo de cumplimiento sería **más del doble de todos los ingresos**.

Con equipos individuales, el modelo no sobrevive al propio reglamento que invoca. Este es el argumento más fuerte que tienen para justificar el cambio de arquitectura, y sale de cruzar su Excel con el texto del DS 40.

---

## 5. La arquitectura colectiva arregla las dos cosas

Al pasar de un equipo por departamento a **una planta colectiva por edificio**:

**a) El costo de cumplimiento se divide entre 50.** Un análisis mensual por edificio, no por departamento: de US$66 a **US$1,3 por vivienda al mes**. Ver [03-normativa-y-requisitos.md](03-normativa-y-requisitos.md), sección 4.

**b) Baja el costo del hardware por vivienda.** Estanque, bombas, lámpara UV, sensores y controlador se comparten en vez de repetirse 50 veces.

**c) Aparecen dos clientes distintos, en dos momentos distintos.** Esta es la pieza que faltaba:

| | Inmobiliaria | Comunidad / administrador |
|---|---|---|
| Cuándo | En obra, una vez | Todos los meses |
| Qué compra | Equipo instalado | Cumplimiento y operación |
| Por qué compra | Certificación (CES, LEED), diferenciación comercial, y no quedar expuesta si la OGUC hace obligatorio el reúso | Ahorro en la cuenta y cumplir el DS 40 sin contratar a nadie |
| Le importa el payback | **No.** Vende los departamentos y se va | **Sí.** Es quien paga la cuenta |

Esto resuelve la objeción del payback: **a quien le cobran el equipo no le importa el payback, y a quien le importa el payback solo le cobran la suscripción.**

---

## 6. Estructura de precios propuesta

> **Advertencia.** El costo de la planta colectiva es una **estimación escalada desde el prototipo**, no una cotización. Hay que pedir precio real de estanques, UV industrial y bombas antes de presentarlo como dato duro. Lo sólido es la estructura y el orden de magnitud del ahorro.

**Edificio tipo de 50 departamentos:**

| Línea | Valor estimado | Nota |
|---|---|---|
| Costo directo de equipo | ~US$11.000 | Estanque, tren escalado, bombas, válvulas, sensores, controlador |
| Instalación y puesta en marcha | ~US$3.000 | En obra nueva. La doble tubería es costo del constructor |
| **Costo directo total** | **~US$14.000** | US$280 por vivienda |
| **Precio de venta** | **US$28.000** | **US$560 por vivienda** |
| Margen bruto | 50% | Mejor que el 39% del equipo individual |

**Capa recurrente, cobrada a la comunidad:**

| Línea | Valor | Nota |
|---|---|---|
| Suscripción de cumplimiento | **US$150 / mes por edificio** | US$3 por vivienda al mes |
| Ingreso anual | US$1.800 | |
| Costo: análisis mensual CF | US$790 | 12 × CLP 65.787, exigido por art. 43 |
| Costo: plataforma y soporte | ~US$300 | |
| **Margen** | **~US$710 al año por edificio** | 39% |
| Consumibles (cartuchos) | ~US$300 al año aparte | Margen adicional |

**La prueba de que cierra:**

| | Equipo individual (hoy) | Planta colectiva (propuesto) |
|---|---|---|
| Ahorro anual por vivienda | US$76 | US$76 |
| Suscripción anual por vivienda | US$96 | **US$36** |
| **Neto para el cliente** | **−US$19** | **+US$40** |

Pasa de perder plata a ganarla, y además cumple el DS 40 sin contratar a nadie. Esa tabla de tres filas es la lámina.

---

## 7. El TAM hay que recalcularlo

El TAM de US$220M del deck 1 sale de 72.000 viviendas × US$3.000. Con el ticket corregido:

| | Deck 1 | Corregido | Supuesto |
|---|---|---|---|
| Ticket por vivienda | US$3.000 | **US$560** | Planta colectiva por vivienda-equivalente |
| **TAM** (72.000 viviendas nuevas al año, INE 2024) | US$220M | **US$40M / año** | |
| **SAM** (40%: regiones con estrés hídrico) | US$90M | **US$16M / año** | |
| **SOM** (3-5% del SAM en 3-5 años) | US$3-5M | **US$0,5-0,8M / año** | |
| Capa recurrente sobre base instalada | No cuantificada | **US$36 por vivienda al año** | Se acumula con cada instalación |

Es un mercado más chico, pero es el real. Y la capa recurrente **se acumula**: a los 5 años, con 3.000 viviendas instaladas, son US$108.000 al año que no desaparecen.

El manual advierte contra *"declaraciones vagas o supuestos sin respaldo, ya que esto podría debilitar la credibilidad ante los inversores"*. Bajar el TAM voluntariamente y explicar por qué da más credibilidad que defender una cifra inflada.

---

## 8. La caja de los primeros 12 meses

El desembolso real de los meses 1 a 9 es de **US$3.158**, no los US$9.008 del costo económico: la diferencia son las horas del equipo, que nadie paga. Y como los meses 10 a 12 siguen gastando sin vender, el punto más bajo de caja es el **mes 12 con US$5.193**.

El detalle, con las fuentes para cubrirlo, está en [08-necesidad-de-caja.md](08-necesidad-de-caja.md).

---

## 9. Lo que falta cerrar

| Pendiente | Quién | Por qué importa |
|---|---|---|
| Tarifa ESSBIO vigente desde una boleta real | Cualquiera del grupo | Cambia una cifra de 2022 por una actual |
| Cotización de estanque, UV industrial y bombas a escala de edificio | Equipo técnico | Convierte la estimación en dato duro |
| Transcribir las tablas del artículo 36 del DS 40 | Quien tenga el PDF | Vienen como imagen, no se pudieron extraer |
| Precio de Yaku o Ecological | Pedir cotización como cliente | Ancla el precio contra competencia real |
| Verificar el 25% de participación del WC | Equipo | Hoy es supuesto propio sin fuente externa |
| Costo real de instalación en retrofit | Equipo | El Excel usa US$65; Hydraloop reporta US$2.000-6.000 en vivienda existente |

---

## Fuentes

- [Aviso de tarifas de agua potable y alcantarillado, ESSBIO S.A.](https://www.essbio.cl/get-files/VTJGc2RHVmtYMStsaWZCK2hoU0szb2dlcVdod2cxTE11OHByU0REdUR0dkxkbUFQb094SmNuRStNVlk5RVZIa0I4ZUNtWUNnOTJrRHFPOXJJcjVwbUlzUjdsRDczVVJyaVlaRjhSVFBaOVU9) — oficial, descargado y leído
- [DS N°40/2024 MINSAL, Diario Oficial](https://www.diariooficial.interior.gob.cl/publicaciones/2024/05/09/43846/01/2489091.pdf) — artículo 43
- [SISS y tarifa de sobreconsumo, Diario Concepción](https://www.diarioconcepcion.cl/economia/2021/12/18/siss-explica-como-evitar-la-tarifa-de-sobreconsumo-de-agua-en-verano.html)
- [Hydraloop H300, Home Unplugged](https://homeunplugged.com/product/hydraloop-h300/) y [costos de instalación, WaterWise Group](https://waterwisegroup.com/blogs/greywater-education/best-greywater-system)
- Consumo por persona y litros por uso: deck 1, láminas 5 y 7
- Costos variables a volumen, precio, plan de mantención y precio Agrolab: Excel del grupo
