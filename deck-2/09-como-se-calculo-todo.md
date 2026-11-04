# Cómo se calculó cada número del deck

Todo lo de acá se puede reproducir con una calculadora. Cada cifra dice de dónde sale: si es dato de fuente externa, supuesto propio del equipo, o estimación sin cotizar.

**Supuesto de conversión usado en todo el documento:** 1 USD = 1.000 CLP. Es el que ya traía el Excel del grupo.

---

## 1. Ahorro de agua: US$76 por vivienda al año

### Los insumos

| Dato | Valor | Origen |
|---|---|---|
| Consumo por persona | 170 L/día | Deck 1, lámina 5. Fuente original: Corporación Ciudades |
| Personas por hogar | 4 | **Supuesto del equipo** |
| Participación del WC en el consumo | 25% | **Supuesto propio**, del resumen del Excel del grupo. Sin fuente externa |
| Tarifa agua potable | 540,81 $/m³ | Aviso oficial ESSBIO, Grupo 1 Cuenca Bío Bío |
| Tarifa alcantarillado | 707,21 $/m³ | Idem. Incluye tratamiento de aguas servidas |

Concepción aparece listada explícitamente en el Grupo 1 Cuenca Bío Bío del aviso, junto con Chiguayante, Penco, San Pedro, Talcahuano, Coronel, Lota y Tomé.

### La cuenta

```
Consumo del hogar   = 170 L × 4 personas × 30 días = 20.400 L = 20,4 m³/mes
Demanda del WC      = 20,4 × 0,25                  = 5,1 m³/mes
Tarifa combinada    = 540,81 + 707,21              = 1.248,02 $/m³
Ahorro mensual      = 5,1 × 1.248,02               = $6.365
Ahorro anual        = $6.365 × 12                  = $76.379  →  US$76
Por edificio de 50  = US$76 × 50                   = US$3.819
```

### El punto que hay que saber defender

**¿Por qué se suma el alcantarillado si el agua igual termina en la alcantarilla?**

Porque en Chile el alcantarillado **se factura sobre el agua potable medida**, no sobre la descarga real. Si el hogar compra menos agua potable, bajan las dos líneas de la boleta. Por eso el ahorro es de 1.248 $/m³ y no de los 541 $/m³ del agua potable sola.

### Verificación de que alcanza el agua gris

No basta con que el WC demande 5,1 m³: hay que tener esa agua gris disponible.

```
Ducha: 80 a 120 L por uso (deck 1, lámina 7)
4 personas × 1 ducha/día × 80 a 120 L = 320 a 480 L/día = 9,6 a 14,4 m³/mes
```

Hay entre **2 y 3 veces más agua gris que demanda de WC**. El cuello de botella es cuánta se puede reutilizar, no cuánta hay. Eso simplifica el diseño: el sistema se dimensiona por el WC y el excedente se va al alcantarillado.

---

## 2. Por qué el cliente perdía plata en el modelo anterior

```
Ahorro del cliente       = US$76,4 / 12 = US$6,36 al mes
Mantención que se cobraba= US$8,00 al mes   (supuesto 2 del plan de crecimiento del grupo)
Resultado                = 6,36 − 8,00     = −US$1,64 al mes
Al año                   = −1,64 × 12      = −US$19,6
```

**El cliente perdía unos US$20 al año por tener Graria**, antes de contar los US$320 del equipo. Ese número salió de cruzar el precio que el propio grupo había puesto con la tarifa real, y es lo que confirma con cifras lo que dijo el supervisor técnico sobre el B2C.

Con la planta colectiva:

```
Suscripción = US$150 al mes ÷ 50 viviendas = US$3,00 al mes por vivienda
Resultado   = 6,36 − 3,00 = +US$3,36 al mes = +US$40,4 al año
```

---

## 3. Costo de cumplimiento: de US$789 a US$16 por vivienda

### De dónde sale el precio del análisis

**CLP 65.787** por análisis de coliformes NMP, laboratorio Agrolab. Es una línea del propio costeo del grupo, en la hoja *Mis primeros 9 meses* del Excel. No es un número inventado para este argumento.

### Por qué es mensual y por sistema

**DS 40, artículo 43:** los sistemas que desinfectan por un proceso distinto a la cloración (la UV lo es) quedan eximidos de medir cloro libre residual, pero deben verificar la calidad bacteriológica del efluente **con frecuencia mensual**. La obligación recae sobre el sistema instalado, no sobre la empresa.

### La cuenta

```
Análisis            = CLP 65.787 = US$65,79

Un equipo por departamento:
  por vivienda al año = 65,79 × 12            = US$789

Una planta por edificio de 50 departamentos:
  por vivienda al mes = 65,79 ÷ 50            = US$1,32
  por vivienda al año = 1,32 × 12             = US$16
```

La razón entre ambos es exactamente 50, que es el número de departamentos que comparten el análisis. No hay magia: es una división.

### El número que hizo parar todo

```
Clientes con mantención activa al mes 48 (plan original) = 1.064
Costo de cumplimiento = 1.064 × US$65,79        = US$70.000 al mes
Ingresos totales del mes 48 (plan original)     = US$30.912 al mes
Razón                 = 70.000 ÷ 30.912         = 2,3 veces
```

Con equipos individuales, cumplir el reglamento costaría **más del doble de todos los ingresos**. Ambas cifras (los 1.064 clientes y los US$30.912) salen de la hoja *Mi plan de crecimiento* del Excel original.

> **Corrección de redondeo.** En una versión anterior del deck decía US$792 y US$70.224, usando US$66 por análisis. Lo correcto con CLP 65.787 es **US$789** y **US$70.000**. Ya está corregido.

---

## 4. Necesidad de caja: US$5.193 en el mes 12

### Separar la caja de las horas

El Excel sumaba en una sola línea el desembolso real y las horas del equipo valorizadas. Para sacar la caja real se resta, mes a mes, la fila *Recursos humanos* (US$650 al mes) de la fila *Egresos*:

| Mes | Egresos totales | − Horas | = Caja real |
|---|---|---|---|
| 1 | 789,79 | 650 | 139,79 |
| 2 | 903,01 | 650 | 253,01 |
| 3 | 682,79 | 650 | 32,79 |
| 4 | 713,78 | 650 | 63,78 |
| 5 | 662,10 | 650 | 12,10 |
| 6 | 750,95 | 650 | 100,95 |
| 7 | 2.468,59 | 650 | 1.818,59 |
| 8 | 943,42 | 650 | 293,42 |
| 9 | 1.093,75 | 650 | 443,75 |
| | | **Total** | **3.158,18** |

**Verificación cruzada:** el propio resumen del Excel dice *"USD 3.158 en materiales y servicios"*. Coincide, así que la separación está bien hecha.

El mes 7 se dispara porque ahí se compran las 5 réplicas, después de validar la integración.

### Por qué el fondo es el mes 12 y no el 9

Los meses 10, 11 y 12 siguen gastando sin vender nada, y la CORFO llega recién el mes 13:

| Mes | En qué se gasta | Cuenta | Total |
|---|---|---|---|
| 10 | Diseño para fabricación | 300 + 50 + 100, más 10% de imprevistos (45) | 495 |
| 11 | Diseño para fabricación | igual | 495 |
| 12 | Certificación de calidad en laboratorio | 800 + 50 + 100, más 10% (95) | 1.045 |
| | | **Subtotal** | **2.035** |

Los imprevistos son el 10% de operaciones más gastos, que es la convención del propio Excel del grupo.

```
Caja al fin del mes 9  = −3.158
Meses 10 a 12          = −2.035
Necesidad máxima       = −5.193  ← en el mes 12
```

### Lo que le toca a cada uno

```
Por persona           = 5.193 ÷ 6 fundadores        = US$866
Por persona al mes    = 866 ÷ 12 meses              = US$72
```

---

## 5. Precio de US$560 por vivienda

**Esta es la cifra más débil del deck y hay que decirlo si preguntan.**

```
Costo de equipo estimado para 50 deptos   ≈ US$11.000
Instalación y puesta en marcha            ≈ US$3.000
Costo directo total                       ≈ US$14.000  →  US$280 por vivienda
Precio = 2 × costo                        = US$28.000  →  US$560 por vivienda
Margen bruto                              = 50%
```

**Es una estimación escalada desde el prototipo, no una cotización.** Está pendiente pedir precio real de estanque, UV industrial y bombas a escala de edificio.

Lo que sí ancla el número es el benchmark: **Hydraloop instalado cuesta entre US$8.000 y US$16.000 por vivienda**. US$560 queda muy por debajo, lo que es coherente con que compartimos una planta entre 50 departamentos en vez de poner un equipo por casa.

### La suscripción

```
Costo: análisis mensual                  = US$66
       plataforma y soporte              = US$25
       total                             = US$91 al mes por edificio
Precio                                   = US$150 al mes por edificio
Margen                                   = US$59 al mes = 39%
Por vivienda                             = 150 ÷ 50 = US$3 al mes
```

---

## 6. TAM, SAM y SOM

```
Viviendas nuevas al año en Chile = 72.000      (INE 2024, ya venía del deck 1)
TAM = 72.000 × US$560                          = US$40M al año
SAM = 40% del TAM                              = US$16M al año
SOM = 3 a 5% del SAM                           = US$0,5 a 0,8M al año
```

El 40% del SAM corresponde a las regiones con estrés hídrico y proyectos sustentables, que es el mismo criterio que usaba el deck 1. Lo único que cambió es el ticket.

### Por qué bajó el TAM

El deck 1 usaba un ticket de US$3.000 por vivienda, de donde salía el TAM de US$220M. Ese ticket no resiste el cálculo de recuperación:

```
US$3.000 ÷ US$76 de ahorro al año = 39,5 años de payback
```

Nadie compra algo que se paga en 39 años. Bajamos el TAM a propósito, y eso es más defendible que sostener una cifra inflada.

Para contexto, Hydraloop: US$8.000 a 16.000 ÷ 76 = **105 a 210 años**. Por eso el importado no penetra el mercado residencial chileno.

---

## 7. Plan de crecimiento: 41 edificios al mes 48

El ritmo de venta es un **objetivo, no un pronóstico**:

| Meses | Ritmo | Edificios |
|---|---|---|
| 13 a 18 | 1 cada 3 meses | 2 |
| 19 a 24 | 1 cada 2 meses | 3 |
| 25 a 36 | 1 por mes | 12 |
| 37 a 48 | 2 por mes | 24 |
| | **Total** | **41** |

41 edificios × 50 viviendas = **2.050 viviendas**. Contra un TAM de 72.000 viviendas al año, eso es alrededor del 1,7% del mercado anual en el cuarto año. Es ambicioso pero no absurdo.

De ahí en adelante todo sale de las fórmulas del Excel: flujo positivo sostenido desde el **mes 25** y caja acumulada de **US$455.198** al mes 48.

---

## 8. Lo que hay que reconocer si lo preguntan

| Cifra | Qué tan firme es |
|---|---|
| Tarifa de 1.248 $/m³ | **Firme**, de aviso oficial de ESSBIO. Pero es de 2022: el ahorro real hoy es mayor |
| Ahorro de US$76 | Firme en aritmética, **apoyado en dos supuestos propios**: 4 personas por hogar y 25% de WC |
| El 25% del WC | **Supuesto propio sin fuente externa.** Es el más flojo de los insumos |
| CLP 65.787 del análisis | **Firme**, es una cotización que el propio grupo levantó |
| Art. 43 del DS 40 | **Firme**, texto oficial del Diario Oficial |
| US$3.158 de caja | **Firme**, se verifica contra el propio resumen del Excel |
| US$5.193 de necesidad | **Firme**, suma directa de las dos anteriores |
| US$560 por vivienda | **Estimación sin cotizar.** Hay que decirlo antes de que lo pregunten |
| 41 edificios al mes 48 | **Objetivo, no pronóstico** |

**La mejora más rápida que pueden hacer:** que alguien fotografíe su boleta de ESSBIO y saque el $/m³ vigente. Cambiar una cifra de 2022 por una de este mes, citando la boleta, sube la calidad de toda la sección financiera por diez minutos de trabajo.
