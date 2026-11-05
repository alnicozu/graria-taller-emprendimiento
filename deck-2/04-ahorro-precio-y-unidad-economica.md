# Modelo de negocio y unidad económica

**La aritmética de cada cifra está en [09-como-se-calculo-todo.md](09-como-se-calculo-todo.md).** Este documento explica el modelo: a quién se le vende, qué paga cada uno y por qué cierra.

Modelo vigente: **equipo por casa, vendido por lote a constructoras en obra nueva, con cloración.**

---

## 1. Dos clientes, dos momentos

| | La constructora | El hogar |
|---|---|---|
| **Cuándo** | Una vez, en obra | Todos los meses, desde que se entrega la casa |
| **Qué compra** | El equipo instalado | El cumplimiento y la operación |
| **Qué paga** | **US$480 por casa** | **US$4 al mes** |
| **Por qué compra** | Suma certificación sustentable al proyecto, entra en los planos sin obra civil extra, y le da un atributo que el comprador entiende: la cuenta del agua baja | Ahorra US$167 al año y no tiene que medir cloro cada semana ni llevar un registro a mano |
| **Le importa el payback** | No. Vende la casa y se va | Sí, pero no lo paga él: va dentro del precio de la vivienda |

**La venta es por proyecto, no por casa.** Un loteo de 80 casas son 80 equipos de una vez: US$38.400 en una sola operación comercial. Eso es lo que hace viable el costo de venta, y es lo que el supervisor técnico señaló cuando dijo que vender casa por casa se come el margen.

---

## 2. Por qué la casa y no el departamento

Esta es la decisión que ordena todo el modelo.

| | Departamento | Casa con jardín |
|---|---|---|
| Dónde se reutiliza | Solo descarga de WC | **WC más riego** |
| Agua reutilizada | 5,10 m³/mes | **8,85 m³/mes** |
| Ahorro anual | US$96 | **US$167** |
| Payback a US$480 | 5,0 años | **2,9 años** |

Un departamento produce entre 9,6 y 14,4 m³ de agua gris al mes y solo puede usar 5,10. **El resto se bota.** La casa tiene dónde ponerla.

El espacio del baño también ayuda, pero menos de lo que parece: baja unos **US$20 de los US$195** del costo, en la partida de hidráulica e instalación, porque el equipo va en la logia y no necesita chasis a medida. Las partidas de electrónica, filtración y despacho no cambian con el tamaño del baño.

---

## 3. La unidad económica

```
VENTA, por casa
  Precio instalado                 US$480
  Costo variable a volumen         US$175
  Margen bruto                     US$305  (64%)

RECURRENTE, por casa al año
  Suscripción de cumplimiento      US$48
  Costo (reactivos, cartuchos, plataforma)  US$28
  Margen                           US$20   (42%)

PARA EL HOGAR, al año
  Ahorra                           US$167
  Paga                             US$48
  Le quedan                        US$119
```

> El costo de US$175 es **estimación escalada desde el prototipo, no cotización**. Pendiente cotizar el dosificador y el sensor de cloro en línea, que son lo único del tren sin precio firme.

**Por proyecto de 80 casas:** US$38.400 de venta, US$24.400 de margen bruto, más US$3.840 al año de recurrente que se acumula con cada proyecto entregado.

---

## 4. El tamaño del mercado

```
Viviendas nuevas autorizadas en Chile, 2025 = 69.058   (INE, vía CChC)
```

Son un 19,7% menos que en 2024 y el nivel más bajo en 34 años, lo que conviene reconocer: **el mercado se está contrayendo**, no creciendo.

| | Valor | Estado |
|---|---|---|
| Ticket por casa | US$480 | Estimado |
| Universo de vivienda nueva | 69.058 al año | **Dato INE 2025** |
| Mercado si se equipara toda la vivienda nueva | **US$33M al año** | Cálculo |
| **Fracción que son casas y no departamentos** | **Por determinar** | ⚠️ **Pendiente: sacarlo del INE** |

**Esta es la cifra que falta.** El TAM del segmento es 69.058 × (fracción casas) × US$480, y esa fracción no está publicada en las fuentes revisadas. Hay que sacarla de los Geodatos Abiertos del INE o del formulario de edificación. Sin ese dato, el dimensionamiento del segmento no se puede cerrar.

> El deck 1 declaraba un TAM de US$220M con un ticket de US$3.000. Ese ticket implicaba un payback de 31 años, así que no se sostenía. Bajar el mercado a propósito, explicando por qué, es más defendible que mantener una cifra inflada.

---

## 5. Lo que falta cerrar

| Pendiente | Por qué importa |
|---|---|
| **Desglose casas / departamentos del INE** | Sin eso no se puede dimensionar el segmento |
| **Cotizar dosificador y sensor de cloro en línea** | Es lo único del tren sin precio firme |
| Fuente externa para el 25% del WC y para el riego | De ahí cuelga todo el ahorro |
| Precio de Yaku o Ecological | Ancla el precio contra competencia real |
| Respaldo mejor para el umbral de cloro en plantas | Hoy viene de literatura divulgativa |

---

## Fuentes

- [Tarifas ESSBIO publicadas el 23-09-2026](https://www.essbio.cl/) — aportadas por el equipo
- [Permisos de edificación 2024, INE](https://www.ine.gob.cl/sala-de-prensa/prensa/general/noticia/2025/05/22/permisos-de-edificaci%C3%B3n-disminuyeron-0-8-en-2024) y [cifra 2025 vía CChC](https://www.biobiochile.cl/noticias/economia/actualidad-economica/2026/02/12/alarmante-gremio-de-la-construccion-advierte-que-permisos-de-edificacion-tocaron-minimos-historicos.shtml)
- [DS N°40/2024 MINSAL, Diario Oficial](https://www.diariooficial.interior.gob.cl/publicaciones/2024/05/09/43846/01/2489091.pdf) — arts. 8, 43 y 45
- [Hydraloop H300, Home Unplugged](https://homeunplugged.com/product/hydraloop-h300/) — referencia de precio
- Costos variables y precio de análisis: Excel del grupo
