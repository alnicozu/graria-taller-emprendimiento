# Correcciones al deck 1, lámina por lámina

El deck 1 ([Presentación 1.pdf](../modulo-1/deck-1/Presentacion-1.pdf), 21 láminas, septiembre 2026) es la base del documento final. Estas son las correcciones que necesita para quedar alineado con lo decidido después.

**Prioridad:** las marcadas con 🔴 son errores que un revisor puede detectar en una pregunta. Las 🟡 son desalineaciones con el diseño actual.

---

> ## ✅ YA APLICADAS
>
> Las correcciones de abajo **ya están hechas** sobre el .pptx del grupo. El archivo corregido es [DECK-1-corregido.pptx](../modulo-1/deck-1/DECK-1-corregido.pptx) y el original quedó guardado como [DECK-1-original.pptx](../modulo-1/deck-1/DECK-1-original.pptx).
>
> Se cambiaron **32 textos en 8 láminas**, editando el XML directamente para no tocar ni el diseño ni las imágenes.
>
> **Lo que falta:** nadie ha visto el archivo renderizado. En este equipo no hay LibreOffice ni pdftoppm, así que no pude revisar si algún texto se desborda de su caja. Abran el .pptx y miren las láminas 6, 13 y 19, que son donde el texto nuevo quedó algo más largo que el original.

---

## 🔴 Lámina 6 — "El problema golpea a toda la cadena"

**Dice:** *"La nueva normativa exige reutilizar aguas grises, pero muchas no saben cómo cumplir ni cómo demostrarlo ante la autoridad."*

**Problema:** la Ley 21.075 **no obliga** a reutilizar. Regula a quien quiera hacerlo. Su artículo 14 delega en la OGUC la definición de qué edificaciones estarán obligadas, y eso todavía no ocurre.

**Reemplazo propuesto:**

> La normativa ya permite reutilizar y fija cómo hacerlo, pero exige autorización sanitaria, parámetros de calidad por uso y registro permanente de autocontrol. Muchas inmobiliarias no saben cómo cumplir ni cómo demostrarlo ante la autoridad, y la OGUC puede volverlo obligatorio en cualquier momento.

Queda igual de fuerte y además resiste la pregunta.

---

## 🔴 Lámina 12 — "Cómo calculamos el mercado"

**Dice:** *"Ticket promedio conservador de ~US$3.000 por vivienda-equivalente"*.

**Problema:** con un ahorro real de US$76 al año por vivienda, ese ticket implica un payback de **39 años**. Y es la base del TAM de US$220M de la lámina 11, así que arrastra todo el dimensionamiento.

**Reemplazo:** ticket de **US$560 por vivienda-equivalente** en planta colectiva. TAM US$40M, SAM US$16M, SOM US$0,5-0,8M al año, más la capa recurrente. Cálculo completo en [04-ahorro-precio-y-unidad-economica.md](04-ahorro-precio-y-unidad-economica.md), sección 6.

Bajar el TAM voluntariamente y explicar por qué da más credibilidad que defender una cifra inflada. El manual advierte contra *"supuestos sin respaldo"*.

---

## 🔴 Lámina 11 — Dimensionamiento TAM / SAM / SOM

Consecuencia directa de la anterior. Hay que rehacer las tres cifras con el ticket corregido.

Vale la pena **mantener la estructura y la fuente** (72.000 viviendas nuevas al año, INE 2024), que están bien. Solo cambia el multiplicador.

---

## 🟡 Láminas 16 y 17 — La solución y cómo funciona

**Dicen:** *"prefiltro + membrana + separación electrostática"*.

**Problema:** el Excel de costeo ya no incluye separación electrostática, y el supervisor pidió simplificar el tren. Además la electrostática exige 3.000 a 9.000 V DC, lo que choca con la promesa de "operación a bajo voltaje" de la lámina 18.

**Reemplazo:** prefiltro de sólidos → microfiltración con carbón activado → desinfección → estanque → reutilización.

En la lámina 17, el bloque "Capa inteligente" sigue sirviendo, pero conviene reformularlo: en vez de "genera el dashboard", decir que **registra la evidencia que el artículo 44 del DS 40 exige mantener disponible para los fiscalizadores**.

---

## 🟡 Lámina 18 — "Por qué es difícil de replicar"

**Dice:** *"Base de datos histórica que mejora con IA por cada instalación"*.

**Problema:** el supervisor dijo que no hace falta IA para este uso del agua. Sostenerlo invita a una pregunta incómoda sobre qué hace exactamente esa IA.

**Reemplazo:** el diferenciador no es la IA, es el **cumplimiento automatizado**. Ningún competidor chileno (Yaku, Ecological, Assa, Ecocontenedores) se posiciona ahí. Ver [02-competencia.md](02-competencia.md).

Mantener sí la idea de defensibilidad por base instalada, pero con otro argumento: cada edificio instalado genera historial de cumplimiento que la comunidad no quiere perder al cambiar de proveedor.

---

## 🟡 Lámina 19 — Focos de trabajo

**Dice:** *"Nuevos segmentos y salto a B2C"* como foco de repetibilidad.

**Reemplazo:** el salto a B2C está descartado por ahora. El foco de repetibilidad pasa a ser **replicar el modelo entre inmobiliarias y hacia municipios (B2G)**.

También en esa lámina, el modelo de ingresos: hoy dice "suscripción de monitoreo, plan anual". Conviene precisarlo como **suscripción de cumplimiento, US$150 al mes por edificio**, y aclarar que la paga la comunidad, no la inmobiliaria.

---

## 🟡 Lámina 13 — Panorama competitivo

**Dice:** compara categorías abstractas ("no hacer nada", "sistemas importados", "ingeniería a medida").

**Problema:** el punto 2 del correo pide *"soluciones o startups que ya existan, con datos concretos"*.

**Reemplazo:** matriz de atributos por empresa con nombres reales. Hay una propuesta lista en [02-competencia.md](02-competencia.md), sección 4. Como mínimo tiene que aparecer **Yaku**, que es el competidor chileno directo.

---

## 🟢 Lo que queda igual

Para que quede claro cuánto se conserva:

| Lámina | Por qué se mantiene |
|---|---|
| 1 a 5 | El problema y la crisis hídrica están bien respaldados, con fuentes citadas |
| 7 | Fuentes de agua gris y usos no potables. Los datos de litros por uso se usan en el cálculo de ahorro |
| 8 a 10 | **La lámina 9 es clave**: ya decía B2B núcleo, municipios y B2C como expansión futura. La lámina 10 (quién paga, quién usa, qué decide) se vuelve más fuerte con la arquitectura colectiva |
| 14 | "Por qué ahora" sigue válida. Solo ajustar el matiz de obligatoriedad de la línea 2018 |
| 15 | *"No vendemos un filtro: vendemos agua reutilizable respaldada por datos que prueban su cumplimiento"*. Esta frase ya era correcta y ahora tiene el DS 40 detrás |
| 20 a 21 | Cierre. Actualizar solo la cifra del SAM |

---

## Resumen

De 21 láminas: **3 con errores que hay que corregir**, 4 desalineadas con el diseño actual, y 14 que quedan como están.

No es rehacer el deck. Es corregir siete láminas y agregar las nuevas del Módulo 2.
