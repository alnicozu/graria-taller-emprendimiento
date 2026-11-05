# Cómo se calculó cada número del deck

Modelo vigente: **equipo por casa, vendido por lote a constructoras en obra nueva, con cloración.**

Todo lo de acá se puede reproducir con una calculadora. Cada cifra dice de dónde sale: dato de fuente externa, supuesto propio del equipo, o estimación sin cotizar.

**Conversión usada en todo el documento:** 1 USD = 1.000 CLP, el supuesto que ya traía el Excel del grupo.

---

## 1. Ahorro de agua: US$167 por casa al año

### Los insumos

| Dato | Valor | Origen |
|---|---|---|
| Consumo por persona | 170 L/día | Deck 1, lámina 5. Fuente original: Corporación Ciudades |
| Personas por hogar | 4 | **Supuesto del equipo** |
| Participación del WC | 25% | **Supuesto propio**, del Excel del grupo. Sin fuente externa |
| Riego de un jardín de 50 m² | 3,75 m³/mes | **Supuesto propio**, promediado al año |
| Agua potable, no punta | 692,20 $/m³ | Tarifas ESSBIO publicadas el **23-09-2026** |
| Alcantarillado con tratamiento | 883,93 $/m³ | Idem |
| Cargo fijo | 944,00 $/mes | Idem. **No entra**: no cambia con el consumo |

### La cuenta

```
Consumo del hogar    = 170 L × 4 personas × 30 días  = 20.400 L = 20,4 m³/mes
Descarga de WC       = 20,4 × 0,25                   = 5,10 m³/mes
Riego del jardín                                      = 3,75 m³/mes
Agua reutilizada     = 5,10 + 3,75                   = 8,85 m³/mes
Tarifa combinada     = 692,20 + 883,93               = 1.576,13 $/m³
Ahorro mensual       = 8,85 × 1.576,13               = $13.949
Ahorro anual         = $13.949 × 12                  = $167.393  →  US$167
```

### Por qué la casa gana al departamento

Un departamento solo puede reutilizar en el WC: **5,10 m³/mes → US$96 al año**. El resto del agua gris que produce se va al alcantarillado porque no tiene dónde usarla.

La casa riega, así que aprovecha **8,85 m³/mes → US$167 al año**. El jardín aporta **US$71 al año**, que es el 42% del total.

### Verificación de que alcanza el agua gris

```
Ducha: 80 a 120 L por uso (deck 1, lámina 7)
4 personas × 1 ducha/día × 80 a 120 L = 320 a 480 L/día = 9,6 a 14,4 m³/mes
```

Se reutilizan 8,85 de los 9,6 a 14,4 disponibles. **Alcanza, con holgura en el rango alto.** El límite es cuánta se puede usar, no cuánta hay.

### Los dos puntos que hay que saber defender

**¿Por qué se suma el alcantarillado si el agua igual termina ahí?** Porque en Chile el alcantarillado **se factura sobre el agua potable medida**, no sobre la descarga real. Si el hogar compra menos agua potable, bajan las dos líneas de la boleta.

**¿Y el sobreconsumo?** En verano la tarifa sobre cierto umbral sube a 1.515,87 $/m³ solo en agua potable. Un hogar que caiga ahí ahorra más. No está contado: es margen a favor.

---

## 2. Payback de 2,9 años

```
Precio del equipo instalado  = US$480
Ahorro anual                 = US$167
Payback                      = 480 ÷ 167 = 2,9 años
```

Esto responde directamente la observación de que **baño por baño saldría muy caro**. Comparado con lo que el profesor vio en el deck 1:

| | Deck 1 | Hoy |
|---|---|---|
| Precio por vivienda | US$3.000 | **US$480** |
| Ahorro anual | US$76 (solo WC, tarifa 2022) | **US$167** (WC + jardín, tarifa vigente) |
| **Payback** | **31 años** | **2,9 años** |

Para contexto: Hydraloop instalado cuesta entre US$8.000 y US$16.000 por vivienda, o sea **48 a 96 años** de payback. Por eso el importado no penetra el mercado residencial chileno.

---

## 3. Cloración en vez de UV: la decisión que dicta el reglamento

### El umbral

```
Agua gris tratada por casa = 8,85 m³/mes ÷ 30 = 0,30 m³/día
Umbral del DS 40, art. 8 letra s              = 1,5 m³/día
```

Estamos muy por debajo, así que el equipo es un **sistema domiciliario de menor tamaño**. Y ahí el reglamento se bifurca según cómo se desinfecte.

### Las dos ramas

| | Con UV | Con cloración |
|---|---|---|
| Artículo que aplica | **43** | **45** |
| Qué exige | Verificación bacteriológica **mensual** de laboratorio, por sistema | Medición **semanal** de cloro libre residual, con equipo portátil |
| Costo | CLP 65.787 × 12 = **US$789 al año por casa** | Reactivos, **~US$15 al año** |
| Veredicto | Más caro que el equipo. Inviable | Viable |

El precio del análisis (CLP 65.787, laboratorio Agrolab) es una línea del propio costeo del grupo, no un número traído para este argumento.

### Lo que el art. 45 también exige

> *"manteniendo registro ordenado de las mediciones realizadas"*

Nadie quiere medir cloro todos los sábados y anotarlo en un cuaderno. **Eso es lo que el producto automatiza**, y por eso la capa de datos no es un adorno: es la respuesta a una obligación legal que recae sobre el dueño de casa (art. 5).

### El contra, que hay que reconocer

El cloro residual va al riego. Según la literatura revisada: **bajo 1 mg/L no afecta el follaje**, y sobre 5 mg/L hay daño severo si se riega por aspersión. La meta del diseño es mantenerlo entre **0,3 y 1,0 mg/L** y regar por goteo, que el art. 41 permite. **No sirve para huerta.**

---

## 4. Necesidad de caja: US$5.193 en el mes 12

*(Sin cambios respecto del modelo anterior: los meses 1 a 12 son los mismos.)*

### Separar la caja de las horas

El Excel sumaba en una sola línea el desembolso real y las horas valorizadas. Para sacar la caja real se resta, mes a mes, la fila *Recursos humanos* (US$650/mes) de la fila *Egresos*:

| Mes | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | Total |
|---|---|---|---|---|---|---|---|---|---|---|
| Egresos | 789,79 | 903,01 | 682,79 | 713,78 | 662,10 | 750,95 | 2.468,59 | 943,42 | 1.093,75 | |
| − Horas | 650 | 650 | 650 | 650 | 650 | 650 | 650 | 650 | 650 | |
| **Caja real** | 139,79 | 253,01 | 32,79 | 63,78 | 12,10 | 100,95 | 1.818,59 | 293,42 | 443,75 | **3.158,18** |

**Verificación cruzada:** el propio resumen del Excel dice *"USD 3.158 en materiales y servicios"*. Coincide. El mes 7 se dispara porque ahí se compran las 5 réplicas.

### Por qué el fondo es el mes 12

| Mes | En qué se gasta | Total |
|---|---|---|
| 10 | Diseño para fabricación: 300 + 50 + 100, más 10% (45) | 495 |
| 11 | Igual | 495 |
| 12 | Certificación de calidad: 800 + 50 + 100, más 10% (95) | 1.045 |
| | **Subtotal meses 10-12** | **2.035** |

```
Caja al fin del mes 9  = −3.158
Meses 10 a 12          = −2.035
Necesidad máxima       = −5.193  ← mes 12, antes de que entre la CORFO en el 13
Por persona            = 5.193 ÷ 6 = US$866
Por persona al mes     = 866 ÷ 12  = US$72
```

---

## 5. Precio y márgenes

> **Advertencia: el costo del equipo es una estimación escalada desde el prototipo, no una cotización.**

```
Costo variable a volumen por casa     ≈ US$175
Precio de venta instalado              = US$480
Margen bruto                           = (480 − 175) ÷ 480 = 64%

Por proyecto de 80 casas:
  Venta   = 80 × 480 = US$38.400
  Costo   = 80 × 175 = US$14.000
  Margen  =            US$24.400
```

Los US$175 bajan respecto de los US$195 del plan anterior porque **el equipo va en la logia y no necesita chasis a medida** bajo el vanitorio. Ese es el aporte real del espacio de una casa: unos US$20 de los US$195, en la partida de hidráulica e instalación. Las de electrónica, filtración y despacho no cambian con el tamaño del baño.

### La suscripción

```
Precio   = US$4 al mes por casa = US$48 al año
Costo    = reactivos, cartuchos y plataforma ≈ US$28 al año
Margen   = US$20 al año por casa (42%)

Para el hogar: ahorra 167 − paga 48 = le quedan US$119 al año
```

---

## 6. Plan de crecimiento

El ritmo es un **objetivo, no un pronóstico**:

| Meses | Ritmo | Proyectos |
|---|---|---|
| 13 a 18 | El primero en el mes 15 | 1 |
| 19 a 24 | 2 más | 2 |
| 25 a 36 | 1 cada dos meses | 6 |
| 37 a 48 | 1 por mes | 12 |
| | **Total** | **21 proyectos = 1.680 casas** |

---

## 7. Qué tan firme es cada cifra

| Cifra | Qué tan firme |
|---|---|
| Tarifa de 1.576 $/m³ | **Firme y vigente**, publicada el 23-09-2026 |
| CLP 65.787 del análisis | **Firme**, cotización que el propio grupo levantó |
| Arts. 8, 43 y 45 del DS 40 | **Firme**, texto oficial del Diario Oficial |
| US$3.158 de caja y US$5.193 de necesidad | **Firmes**, se verifican contra el Excel |
| Ahorro de US$167 | Firme en aritmética, **apoyado en tres supuestos propios**: 4 personas, 25% de WC y 3,75 m³ de riego |
| El 25% del WC y los 3,75 m³ de riego | **Supuestos propios sin fuente externa.** Son los insumos más flojos |
| US$480 de precio y US$175 de costo | **Estimación sin cotizar.** Decirlo antes de que lo pregunten |
| Cloro bajo 1 mg/L sin daño al follaje | De literatura divulgativa, **conviene respaldarlo mejor** |
| 21 proyectos al mes 48 | **Objetivo, no pronóstico** |

### Las tres mejoras más rápidas

1. **Fuente externa para el 25% del WC y para el consumo de riego.** De ahí cuelga todo el ahorro.
2. **Cotizar el dosificador y el sensor de cloro en línea.** Es lo único del tren que no está cotizado.
3. **Conseguir del INE el desglose de casas contra departamentos** en viviendas nuevas, para dimensionar el segmento.

---

## Historial de este documento

| Versión | Qué cambió |
|---|---|
| 1 | Modelo B2C, equipo por departamento, tarifa 2022 |
| 2 | Planta colectiva por edificio, tras la entrevista del 26/10 y el art. 43 |
| 3 | Tarifa vigente del 23-09-2026: el ahorro sube 26% |
| **4 (esta)** | **Casas en obra nueva con cloración**, tras la observación del profesor sobre el costo baño por baño. El jardín casi duplica el ahorro y el payback cae de 31 a 2,9 años |
