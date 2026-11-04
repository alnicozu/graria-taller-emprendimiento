# El deck del Módulo 2

**Link:** https://claude.ai/artifact/UMVRbakcPwBUuavwnDhE97

Es privado: solo lo ve quien lo creó. Para que el resto del grupo lo abra, hay que compartirlo desde el menú **Share** de la propia página. Desde ahí también se descarga como **.pptx** o **PDF**.

Cada lámina trae **notas del orador** con lo que hay que decir, incluidas las respuestas a las preguntas más probables. Se ven en modo presentación.

---

## Las 14 láminas

| # | Lámina | Qué responde |
|---|---|---|
| 1 | Portada | — |
| 2 | **Equipo** | Punto 1 del correo. ⚠️ Tiene placeholders `[Nombre]` y `[Fortaleza o logro]` |
| 3 | Competencia, panorama | Punto 2. Yaku, Ecological, Assa, Ecocontenedores, Hydraloop con datos |
| 4 | Competencia, benchmark | Punto 2. Matriz de atributos, al estilo del ejemplo del profesor |
| 5 | **Iteración** | El eje de la presentación. Qué probamos y qué cambiamos |
| 6 | Tecnología, cómo funciona | Punto 3. Tren de cinco etapas ya simplificado |
| 7 | Tecnología, desafíos | Punto 3. Los tres desafíos con indicador y meta |
| 8 | Normativa y requisitos | Punto 3. Incluye la corrección sobre la obligatoriedad |
| 9 | **El hallazgo del art. 43** | Punto 3. Por qué la arquitectura es colectiva |
| 10 | Propuesta única de valor | Punto 3. Tres clientes, tres beneficios distintos |
| 11 | Unidad económica | Punto 4. Ahorro real y el error que corregimos |
| 12 | Plan financiero | Punto 4. Cuatro años en tres fases |
| 13 | Primeros pasos | Punto 4. Las cuatro etapas con su criterio de éxito |
| 14 | Cierre | — |

Las láminas 5, 9 y 11 son las que cargan el relato. Si hay que recortar tiempo, recortar de las otras.

---

## Lo único que falta llenar

La lámina 2 tiene cuatro tarjetas por función, con placeholders:

| Función | Cuántas personas | Qué poner |
|---|---|---|
| Gestión y finanzas | 1 | Nombre y un logro que respalde el rol |
| Diseño hidráulico | 2 | Nombres y un logro |
| Electrónica y datos | 2 | Nombres y un logro |
| Validación y laboratorio | 1 | Nombre y un logro |

La línea de abajo con los seis fundadores ya está completa.

Si alguien hizo práctica en una constructora o inmobiliaria, **esa es la carta más fuerte del equipo** frente a este jurado, porque el cliente del modelo es justamente la inmobiliaria. Conviene que aparezca.

---

## Antes de presentar

| Qué | Por qué |
|---|---|
| Llenar la lámina 2 | Es el punto 1 de los cinco que evalúa el profesor |
| Llevar la ficha de visado impresa y firmada | Sin eso no se puede presentar |
| Repasar las notas del orador | Traen las respuestas a las preguntas más probables |
| Ensayar el bloque 5-9-11 | Es donde está la profundidad que el profesor dijo que iba a exigir |
| Decidir quién dice qué | El punto 5 incluye "discurso claro y buenas respuestas" |

---

## Diseño

Sigue lo que pide el manual (*"láminas de informe de ingeniería: fondo blanco, más informe que presentación, textos claros, números, autocontenidas"*) y la identidad del deck 1, extraída del propio archivo:

| Elemento | Valor | De dónde sale |
|---|---|---|
| Tipografía | Arial / Arial Bold | Es la del deck 1 (580 usos de Arial Bold, 466 de Arial) |
| Navy principal | `#0C2C46` | El color más usado del deck 1 |
| Texto de cuerpo | `#5C6B74` | Idem |
| Fondos pálidos | `#F2F8FC`, `#EAF3F9` | Idem |
| Acento teal | `#12B0A0` | Idem, y es el del logo |
| Acento azul | `#1E76C4` | Idem, usado en las curvas |
| Acento coral | `#EE6C4D` | Idem, reservado para lo que está mal |

El **logo** va abajo a la derecha en todas las láminas claras, y en versión blanca en las dos oscuras (5 y 14). El original venía con fondo blanco opaco, así que se le quitó el fondo y se escaló 4x. Las dos versiones están en [marca/](../marca/).

### Los gráficos

El profesor observó que el deck 1 era muy plano, sin ayudas visuales. Estas son las cinco que se agregaron:

| Lámina | Gráfico | Qué muestra |
|---|---|---|
| 4 | **Mapa de posicionamiento 2x2** | Estandarización para obra nueva contra evidencia de cumplimiento. El cuadrante superior derecho está vacío y ahí se ubica Graria |
| 6 | **Diagrama de proceso** | Las cinco etapas del tren en línea, con numeración y flechas |
| 9 | **Curva de costo de cumplimiento** | Cómo cae el costo por vivienda, de US$792 a US$16, según cuántos departamentos comparten una planta |
| 11 | **Barras de ahorro contra pago** | Las dos escenas lado a lado: el cliente pierde US$19 o gana US$40 |
| 12 | **Curva de caja, meses 9 a 18** | El descenso hasta −US$5.193 en el mes 12 y la recuperación al entrar la CORFO |
| 13 | **Línea de tiempo de 9 meses** | Las cuatro etapas proporcionales a su duración |

Decisiones de los gráficos, para poder defenderlas:

- **Un solo eje por gráfico.** Nada de dos escalas en un mismo plot.
- **La curva de caja muestra los meses 9 a 18, no los 48.** Con el rango completo (hasta US$455k) el tramo negativo se aplastaría a nada, y ese tramo es justamente el mensaje. Los números del mes 48 van como cifras aparte.
- **El coral está reservado** para lo que está mal o pendiente, nunca como "color de serie".
- Cada cifra lleva su etiqueta directa: el color nunca es el único canal.

> **No se pudo correr el validador de paleta** (`validate_palette.js` necesita Node, que no está en este equipo). Para compensar, ningún gráfico usa más de dos colores de serie a la vez, y nunca se combinan teal y azul como categorías contiguas.

---

## Las láminas del deck 1 que hay que corregir

Este deck es la entrega del Módulo 2 y se suma al del Módulo 1. Las correcciones pendientes del deck 1 están en [05-correcciones-deck-1.md](05-correcciones-deck-1.md): tres errores y cuatro desalineaciones, sobre 21 láminas.
