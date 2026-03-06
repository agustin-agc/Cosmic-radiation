# ☄️ Simulación y análisis de radiación de rayos cósmicos

![Python](https://img.shields.io/badge/Python-3.10-blue)
![CORSIKA](https://img.shields.io/badge/Simulation-CORSIKA-orange)
![ROOT](https://img.shields.io/badge/Data%20Analysis-ROOT-red)
![Physics](https://img.shields.io/badge/Field-Astroparticle%20Physics-green)

En este proyecto desarrollé una herramienta para estudiar la **radiación producida por rayos cósmicos en la atmósfera terrestre**.

El objetivo fue construir un flujo de trabajo que combine **modelos teóricos, simulaciones Monte Carlo y datos experimentales** para estimar la **dosis de radiación cósmica a distintas altitudes**.

1. **Modelo Teórico:**
   Desarrollé un modelo matemático que describe la variación del **flujo de muones con la altitud**, considerando efectos atmosféricos como cambios en la presión y la densidad del aire. A partir de este flujo se propuso una ecuación que fue ajustada a un modelo de cálculo de **dosis de radiación cósmica propuesto por el ISNAP (Institute for Structure and Nuclear Astrophysics)**, utilizándolo como referencia para las estimaciones de dosis.

2. **Simulación Física:**
   Utilicé simulaciones **Monte Carlo con CORSIKA** para modelar las cascadas atmosféricas producidas por rayos cósmicos primarios. Estas simulaciones permiten estimar el **flujo de partículas secundarias** y analizar la fracción relativa de distintos tipos de partículas a diferentes altitudes, con el objetivo de convertir estos flujos en estimaciones de dosis de radiación.

3. **Procesamiento de Datos:**
   Los resultados de las simulaciones fueron analizados utilizando herramientas en **Python y ROOT**, permitiendo identificar las partículas secundarias generadas y estudiar su distribución en función de la altitud.

4. **Recopilación de Datos Experimentales:**
   Se utilizaron **detectores de centelleo acoplados a tubos fotomultiplicadores (Scintillator + PMT)** para medir el flujo de muones a distintas altitudes. Las mediciones se realizaron durante intervalos de al menos **30 minutos en alturas fijas**, con el fin de obtener estimaciones experimentales del flujo de partículas.

5. **Estimación de Dosis:**
   Finalmente, el flujo de muones obtenido fue convertido en **estimaciones de dosis de radiación**, comparando tres enfoques: el modelo teórico desarrollado, los datos experimentales y los resultados obtenidos mediante simulaciones con **CORSIKA**.


# 🔬 Motivación científica

Los rayos cósmicos primarios (principalmente protones de alta energía) interactúan con la atmósfera terrestre produciendo **cascadas de partículas**.

Entre estas partículas destacan los **muones**, que pueden atravesar grandes espesores de materia y llegar hasta la superficie terrestre.

Comprender su flujo permite:

* estudiar la radiación atmosférica
* estimar dosis de radiación en aviación
* validar modelos de interacción hadrónica
* comparar simulaciones con detectores reales

---

# ⚙️ Metodología

El proyecto combina varias etapas.

## 1. Simulación de cascadas atmosféricas

Se utilizan simulaciones **Monte Carlo con CORSIKA** para modelar la interacción de rayos cósmicos con la atmósfera.

Configuración principal:

* Modelo hadrónico de alta energía: **SIBYLL 2.3e**
* Modelo de baja energía: **GHEISHA**
* Geometría atmosférica curva
* Producción explícita de muones

Las simulaciones generan archivos con las partículas secundarias detectadas.

---

## 2. Procesamiento de datos

Los resultados de las simulaciones se analizan usando herramientas en **Python y ROOT** para:

* identificar muones detectados
* calcular el flujo de partículas
* estudiar variaciones con la altitud

---

## 3. Conversión a dosis de radiación

A partir del flujo de muones se estima la **dosis equivalente de radiación** utilizando modelos simplificados de deposición de energía.

Se comparan dos aproximaciones.

**Modelo idealizado**

[
D(h) = 0.0375 \cdot 2^{h/1500}
]

**Modelo basado en simulación**

La dosis se calcula utilizando el flujo simulado de muones y su contribución relativa a la radiación total.

---

# 📊 Resultados esperados

El proyecto permite:

* estudiar cómo varía el flujo de muones con la altitud
* comparar modelos teóricos con simulaciones
* estimar dosis de radiación en vuelos comerciales
* validar simulaciones con datos experimentales

---

# 🧪 Aplicaciones

Este tipo de análisis es relevante en:

* **física de astropartículas**
* **radiación en aviación**
* **monitoreo atmosférico**
* **detectores de rayos cósmicos**

---

# 🚀 Trabajo futuro

* Comparación con datos experimentales usando detectores de centelleo
* Integración con **FLUKA** para cálculos de dosis más precisos
* Extensión del modelo a partículas adicionales (neutrones y electrones)


# 👨‍🔬 Autor

**Agustín Galdames Contreras**  
Licenciado en Física  
Universidad Andrés Bello
