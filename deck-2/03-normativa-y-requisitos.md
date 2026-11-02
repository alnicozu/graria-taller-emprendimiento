# Normativa y requisitos técnicos (DS 40 / Ley 21.075)

Fuente: texto completo del **DS N°40/2024 del Ministerio de Salud**, publicado en el Diario Oficial el 9 de mayo de 2024, y la **Ley N°21.075** (15 de febrero de 2018). Las citas de artículos vienen del texto oficial.

Esta es la base del punto 3 del correo del profesor: *"qué requisitos debe cumplir"*.

---

## 1. Corrección importante: la ley NO obliga a reutilizar

El deck 1 (lámina 6) dice que *"la nueva normativa exige reutilizar aguas grises"*. **Eso no es correcto** y es el tipo de afirmación que se cae en una pregunta.

Lo que dice realmente la Ley 21.075:

- La ley **regula** la recolección, reutilización y disposición de aguas grises. Se aplica a quien **quiera** instalar un sistema.
- Su **artículo 14** encarga a la Ordenanza General de Urbanismo y Construcciones (OGUC) definir en qué edificaciones **será obligatorio** contar con estos sistemas. Mientras la OGUC no lo fije, no hay obligación general.
- La **Ley 21.623** modificó la 21.075 para fomentar la reutilización y ampliar usos al sector silvoagropecuario.
- La ley sí crea un **incentivo tarifario**: modifica el régimen de tarifas para considerar descuentos cuando las aguas grises se recolectan de forma separada.

**Cómo reformularlo sin perder fuerza:**

> La norma todavía no obliga a reutilizar, pero sí define con detalle cómo hacerlo. El que decide reutilizar queda sujeto al DS 40: autorización sanitaria, parámetros de calidad por uso, monitoreo de autocontrol y registro permanente. Ese cumplimiento es caro y engorroso, y es exactamente lo que Graria automatiza. Además, la OGUC puede hacerlo obligatorio en cualquier momento, y ahí el mercado se abre de golpe.

Es más honesto, se sostiene ante una pregunta y conserva el argumento del "por qué ahora".

---

## 2. Usos permitidos (DS 40, artículo 34)

| Uso | Qué incluye |
|---|---|
| **a. Urbanos** | Riego de jardines y **descarga de aparatos sanitarios**: inodoros y urinarios de viviendas, edificios públicos, habitacionales y de actividades económicas |
| b. Recreativos | Riego de áreas verdes públicas, campos deportivos, parques, plazas, áreas de establecimientos educacionales |
| c. Ornamentales | Áreas verdes y jardines sin acceso al público |
| d. Industriales | Procesos no alimenticios y **refrigeración no evaporativa** |
| e. Ambientales | Riego de especies reforestadas, mantención de humedales |
| f. Silvoagropecuarios | Riego de cultivos, salvo los prohibidos en el artículo 9 de la ley |

Los dos usos de Graria (descarga de WC y riego de jardines) caen ambos en la categoría **urbanos**, la más exigente en calidad por el nivel de contacto con personas.

> **Dato para el foco de nuevos usos:** el profesor sugirió explorar el agua para aire acondicionado o refrigeración. El artículo 34 letra d lo permite, pero solo para **refrigeración no evaporativa**. La torre de enfriamiento evaporativa queda fuera. Vale la pena decirlo: muestra que revisaron la norma antes de proponer el uso.

---

## 3. El hallazgo que define la arquitectura del producto

Este es el punto más importante del análisis. El DS 40 impone **tres regímenes de monitoreo distintos**, y la diferencia entre ellos decide si el negocio es viable.

### Artículo 8 letra s, qué es un sistema "de menor tamaño"

Sistemas domiciliarios de pequeños volúmenes que generen un caudal de aguas grises tratadas **menor o igual a 1,5 m³ por día**.

### Artículo 45, régimen de los sistemas de menor tamaño

Solo exige medir **cloro libre residual** en el efluente, en el punto más cercano a la reutilización, con **frecuencia semanal**.

### Artículo 43, la trampa de la desinfección UV

Los sistemas que consideren desinfección por **procesos diferentes a la cloración** quedan eximidos del parámetro Cloro Libre Residual. Pero en esos sistemas *"se deberá verificar la calidad bacteriológica (CF) del efluente tratado con una frecuencia mensual"*.

Traducción: **si usan UV en vez de cloro, cambian una tira reactiva semanal por un análisis de laboratorio mensual.**

### Artículo 44, régimen de los sistemas colectivos

Los sistemas distintos a los de menor tamaño deben tener monitoreo de autocontrol según el artículo 36, **más registro y seguimiento** de los resultados y de los parámetros de control del tratamiento.

---

## 4. Por qué esto mata el equipo por departamento

Usando el precio de análisis del **propio Excel del grupo** (Agrolab, coliformes NMP: **CLP 65.787** por análisis):

| Arquitectura | Caudal | Régimen | Costo de monitoreo |
|---|---|---|---|
| Equipo bajo lavamanos, 1 depto | ~0,3 m³/día | Menor tamaño + UV, art. 43 | **CLP 65.787 al mes por departamento** (≈ US$66) |
| Planta colectiva, 50 deptos | ~15 m³/día | Art. 44, colectivo | **CLP 1.316 al mes por departamento** (≈ US$1,3) |

El equipo por departamento con UV tiene un costo de cumplimiento de **US$790 al año**, más que el equipo completo. Es inviable.

La planta colectiva reparte un solo análisis entre 50 departamentos y **cabe sin problema dentro del plan de mantención de US$8 al mes**.

**La norma, por sí sola, empuja el producto hacia el sistema colectivo de edificio.** Coincide con lo que dijo el supervisor técnico (B2B, no B2C) y con lo que planteaba el deck 1 desde septiembre. Tres fuentes independientes apuntando al mismo lugar.

---

## 5. Y además justifica la capa de datos

El artículo 44 exige *"registro y seguimiento, tanto de los resultados de los análisis de autocontrol de la calidad del efluente generado como de los parámetros de control del sistema de tratamiento"*. El artículo 43 agrega que el registro mensual *"deberá mantenerse ordenado y disponible, en formato físico o digital, para cuando sean requeridos por los organismos fiscalizadores"*.

Eso es, literalmente, lo que hace Graria.

No están vendiendo un dashboard bonito: están vendiendo el cumplimiento de una obligación legal que hoy alguien lleva en una carpeta. Es el argumento de propuesta de valor más fuerte que tienen, y está respaldado por el texto de la norma.

---

## 6. Otros requisitos que el sistema debe cumplir

| Artículo | Requisito |
|---|---|
| 5 | El **titular de la autorización** responde por la calidad del agua tratada desde los artefactos hasta la reutilización, y por la operación y mantención. En edificios en copropiedad se rige además por la Ley 21.442 |
| 6 | Hay que acreditar dominio, posesión o tenencia del inmueble al pedir la autorización |
| 9 | Todo sistema debe contar con un proyecto aprobado |
| 35 | El tratamiento debe ser **acorde al origen y calidad del agua y al uso previsto** (respalda el Foco 3: norte duro contra sur blando) |
| 36 | Define las tablas de calidad por uso. **Pendiente:** las tablas vienen como imagen en el Diario Oficial y no se pudieron extraer. Hay que transcribirlas a mano |
| 37 | En riego, evitar sobresaturación, estancamiento y escurrimiento fuera del área |
| 38 y 40 | **Señalización obligatoria**: letrero "Área Verde Regada con Aguas Grises Tratadas - Agua No Potable" según NCh 1411/1:1978 |
| 39 | Las áreas recreativas solo se riegan cuando están cerradas al público |
| 42 | En usos industriales y ambientales: coliformes fecales **≤ 1.000 NMP/100 mL**, y la Autoridad Sanitaria puede exigir menos |
| 43 | El muestreo de cloro libre residual, turbiedad y coliformes fecales **siempre es puntual** |

---

## 7. La decisión técnica que hay que tomar y documentar

El DS 40 obliga a elegir entre dos caminos de desinfección, y cada uno arrastra un régimen de monitoreo distinto:

| | Cloración | UV (lo que tienen hoy) |
|---|---|---|
| Monitoreo exigido | CLR semanal (art. 45 si es menor tamaño) | **CF de laboratorio mensual** (art. 43) |
| Costo recurrente | Tira reactiva, centavos | CLP 65.787 por análisis |
| Equipo | Dosificador y sensor de CLR | Lámpara UV (US$46 en su Excel) |
| Subproductos | Cloro residual en el agua de riego | Ninguno |
| Encaje con sensores | El sensor de CLR es barato y automatizable | La CF no se mide en línea, requiere laboratorio |

**Recomendación:** en la arquitectura colectiva el costo mensual se diluye y UV sigue siendo viable. Pero hay que **decirlo explícitamente en el deck**, porque es una decisión de diseño tomada a partir de una norma.

Eso es justo lo que pide el componente 6 del visado ABET: *"evidencia de que la norma citada fue efectivamente usada para decidir, no solo nombrada"*. Hoy ese componente está marcado como Logrado; esta sección lo sostiene si se los preguntan.

---

## Fuentes

- [DS N°40/2024 MINSAL, Diario Oficial 9 de mayo de 2024](https://www.diariooficial.interior.gob.cl/publicaciones/2024/05/09/43846/01/2489091.pdf) — texto completo, descargado y leído
- [Ley N°21.075, BCN](https://www.bcn.cl/leychile/navegar?idNorma=1203416)
- [Análisis jurídico del reúso de aguas grises en Chile, Uría](https://www.uria.com/documentos/publicaciones/9041/documento/AJUM-65.pdf)
- [Ley 21.075 regula la recolección, reutilización y disposición de aguas grises, Microjuris](https://aldiachile.microjuris.com/2018/02/15/ley-no-21-075-regula-la-recoleccion-reutilizacion-y-disposicion-de-aguas-grises/)
- [Aguas grises para riego, INDAP](https://www.indap.gob.cl/aguas-grises-para-riego)
