# Automatidata: Análisis Estadístico Inferencial y A/B Testing en NYC Taxi

Proyecto de analítica cuantitativa enfocado en la validación estadística de hipótesis sobre el comportamiento del gasto de los usuarios en los taxis de Nueva York (NYC TLC), verificando supuestos matemáticos rigurosos para la toma de decisiones informada.

---

## 🎯 Contexto y Pregunta de Negocio

El objetivo del proyecto consiste en determinar si existe una diferencia estadísticamente significativa en el importe total de la tarifa (*fare amount*) entre los clientes que abonan con tarjeta de crédito y aquellos que pagan en efectivo.

* **Hipótesis Nula ($H_0$):** No existe diferencia en el importe medio abonado entre los usuarios de tarjeta de crédito y los usuarios de efectivo ($\mu_1 = \mu_2$).
* **Hipótesis Alternativa ($H_A$):** Existe una diferencia estadísticamente significativa en el importe medio abonado según el método de pago ($\mu_1 \neq \mu_2$).
* **Nivel de Significancia ($\alpha$):** 0.05 (5%).

---

## 🔬 Metodología y Validación de Supuestos

Antes de aplicar la prueba inferencial, se evaluaron los supuestos fundamentales:

1. **Análisis Exploratorio de Datos (EDA):** Detección de atípicos, inspección de valores nulos y distribución de frecuencias por método de pago.
2. **Prueba de Normalidad:** Evaluación gráfica y test formal de **Shapiro-Wilk** para verificar el comportamiento de la distribución de las tarifas.
3. **Prueba de Homocedasticidad (Igualdad de Varianzas):** Aplicación del **Test de Levene**, confirmando que las varianzas poblacionales de ambos grupos no son homogéneas.
4. **Selección de la Prueba Estadística:** Debido a la heterocedasticidad observada, se utilizó la **prueba t de Welch** (*Welch's t-test* con varianzas desiguales), garantizando robustez analítica frente a la prueba t de Student tradicional.

---

## 📊 Resultados y Conclusiones de Negocio

* **Estadístico t y p-valor:** El valor de $p$ obtenido fue significativamente menor que el umbral $\alpha = 0.05$, lo que condujo a **rechazar la hipótesis nula ($H_0$)**.
* **Hallazgo Clave:** Los pasajeros que utilizan tarjeta de crédito registran tarifas medias significativamente más altas en comparación con los pagos en efectivo, correlacionado con trayectos de mayor distancia y aeropuertos.
* **Recomendación Estratégica:** Incentivar terminales de pago digital y promociones de tarjeta en trayectos largos para maximizar el ticket promedio y la propina reportada.

---

## 🛠️ Stack Tecnológico

* **Lenguaje:** `Python`
* **Librerías Estadísticas:** `SciPy` (`scipy.stats`), `Statsmodels`
* **Manipulación de Datos:** `Pandas`, `NumPy`
* **Visualización:** `Matplotlib`, `Seaborn`

---

## 📁 Archivos del Repositorio

* `Automatidata project lab`: Jupyter Notebook documentado paso a paso con código reproducible, limpieza, gráficos de distribución y cálculos estadísticos.

---

## 👤 Autor

**Santiago Rodríguez Garay**  
*Lic. en Gestión Turística & Google Certified Advanced Data Analyst*  
* [LinkedIn](https://www.linkedin.com/in/santiago-rodriguez-garay-9b2a3034a)
* [Email](mailto:santiagomanuelrg@gmail.com)
