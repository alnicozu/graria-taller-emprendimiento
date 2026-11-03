# Necesidad de caja de los primeros 12 meses

Este documento responde la retroalimentación que dieron los ayudantes sobre el Excel entregado.

> **Lo que dijeron:**
> *"El costeo está muy bien logrado, cada componente está cotizado y vinculado a su etapa, y la compra de réplicas se condiciona a validar la integración, lo que muestra buen criterio. Lo que más falta es la lectura financiera del flujo. Primero, conviene separar el costo de oportunidad de las horas del gasto en efectivo. Segundo, deben indicar de dónde salen los recursos de los primeros meses: como la CORFO llega recién en el mes 13, la mayor necesidad de caja ocurre en el mes 12, no en el mes 9."*

Las dos observaciones son correctas y ya están aplicadas en [mis-cuentas-VIGENTE-B2B.xlsx](../finanzas/mis-cuentas-VIGENTE-B2B.xlsx), hoja **"Necesidad de caja 1-12"**.

---

## 1. Separar las horas del gasto en efectivo

El plan original mostraba un flujo acumulado de **−US$9.008** al mes 9. Pero esa cifra mezcla dos cosas distintas:

| Concepto | Monto | ¿Sale plata del bolsillo? |
|---|---|---|
| Materiales y servicios de los 9 meses | US$3.158 | **Sí** |
| Horas del equipo valorizadas a $5.000/h | US$5.850 | **No.** Nadie las paga |
| **Costo económico total** | **US$9.008** | — |

El costo de oportunidad sirve para mostrar lo que vale el esfuerzo del equipo, pero **no se financia**. Meterlo en el flujo de caja hace parecer que hace falta el triple de plata de la que realmente se necesita.

En el plan v2 las horas van en una **línea de memoria al final de la hoja**, separadas del flujo de efectivo. La caja del mes 9 cierra en **−US$3.158**, no en −US$9.008.

Las horas dejan de contarse en el mes 16, cuando los fundadores pasan a sueldo y su costo sí se vuelve desembolso.

---

## 2. El verdadero peor momento de caja es el mes 12

Los meses 10, 11 y 12 siguen gastando y todavía no venden nada:

| Mes | En qué se gasta | Monto |
|---|---|---|
| 10 | Diseño para fabricación | US$495 |
| 11 | Diseño para fabricación | US$495 |
| 12 | Certificación de calidad en laboratorio | US$1.045 |
| | **Subtotal meses 10–12** | **US$2.035** |

La Semilla Inicia CORFO entra recién en el **mes 13**. Entonces la caja sigue bajando tres meses más después del prototipo:

| | Caja acumulada |
|---|---|
| Fin del mes 9 | −US$3.158 |
| Fin del mes 10 | −US$3.653 |
| Fin del mes 11 | −US$4.148 |
| **Fin del mes 12** | **−US$5.193** ← punto más bajo |
| Mes 13 (entra CORFO y se vende el primer edificio) | +US$27.182 |

**La necesidad máxima de caja es de US$5.193 y ocurre en el mes 12.** Ese es el número que hay que poder defender, no los US$9.008.

---

## 3. De dónde salen esos US$5.193

| Fuente | Monto | Estado |
|---|---|---|
| **Aporte de los fundadores** | US$5.193 | Es la base y la única fuente segura. Repartido en 12 meses son **US$72 por persona al mes** (6 personas) |
| **Fondo UdeC para startups científico-tecnológicas lideradas por estudiantes**, vía IncubaUdeC | Por confirmar | Entrega financiamiento más acceso al Programa de Preincubación. **Pendiente:** revisar monto y fechas en incubaudec.cl |
| Sercotec Capital Semilla Emprende | CLP 3.500.000 | Exige empresa formalizada y la convocatoria 2026 cerró en mayo. No sirve para esta etapa |
| Semilla Inicia CORFO | US$15.000 | Llega el mes 13. Exige 25% de aporte propio: esos **US$5.000 van aparte** de los US$5.193 |

**Requisito a verificar del fondo UdeC:** exige haber participado antes en programas de innovación de la universidad (Gearbox, Ciencia 2030, IncubaUdeC u otras iniciativas equivalentes). Hay que confirmar si el equipo califica; si no, conviene inscribirse en alguno este semestre para habilitar la postulación.

**Lo honesto para el deck:** el aporte de fundadores es el caso base porque es lo único que no depende de terceros. El fondo UdeC se presenta como la vía para reducirlo, no como un hecho.

---

## 4. Qué cambió en el Excel

El archivo vigente **es el original del grupo editado**, no uno nuevo: conserva sus 5 hojas y sus fórmulas, y suma una sexta.

| Hoja | Qué cambió |
|---|---|
| **Resumen del emprendimiento** | Pasa a B2B y suma la necesidad máxima de caja, su origen y el costo de oportunidad informado aparte |
| **Mis primeros 9 meses** | **Intacta**, con sus 78 líneas cotizadas. Se le agregó abajo un bloque de lectura financiera: egresos en efectivo, caja acumulada real y horas como memoria |
| **Necesidad de caja 1-12** *(nueva)* | Mes a mes del 1 al 12, con el mínimo marcado y las cinco fuentes de financiamiento |
| **Mi plan de crecimiento** | Unidad de venta pasa a edificio. Caja arranca en −3.158, aparece el bloque *Memoria — no es caja* y los imprevistos pasan a ser fórmula |
| **Mis OKRs** | El piloto pasa de 5 hogares a un edificio; las metas se expresan en edificios |
| **Cap Table** | **Sin tocar** |

---

## 5. Esto también responde al profesor

El punto 4 del correo pide *"cómo parte el negocio, qué metas tienen para la primera etapa y cuánto dinero necesitan para ella"*.

La respuesta precisa es **US$5.193, con el peor momento en el mes 12**, no los US$9.008 del costo económico. Está en la lámina 12 del [deck](07-el-deck.md).

Que el equipo haya corregido esto a partir de la retroalimentación de los ayudantes es, además, una iteración documentada más.

---

## Fuentes

- [UdeC lanza fondo para financiar startups científico-tecnológicas lideradas por estudiantes, IncubaUdeC](https://www.incubaudec.cl/udec-lanza-fondo-para-financiar-startups-cientifico-tecnologicas-lideradas-por-estudiantes/)
- [IncubaUdeC ejecutará Ruta Capital, Noticias UdeC](https://noticias.udec.cl/incubaudec-ejecutara-ruta-capital-programa-que-busca-escalar-emprendimientos-tecnologicos/)
- [Capital Semilla Emprende, Portal de Emprendimiento](https://miportalemprendimiento.gob.cl/programas/capital-semilla-emprende)
- Costeo de los meses 1 a 9 y de los meses 10 a 12: Excel del grupo, *Mis cuentas de emprendimiento*
