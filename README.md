# ☄️ Simulación y análisis de radiación de rayos cósmicos

![Python](https://img.shields.io/badge/Python-3.10-blue)
![CORSIKA](https://img.shields.io/badge/Simulation-CORSIKA-orange)
![ROOT](https://img.shields.io/badge/Data%20Analysis-ROOT-red)
![Physics](https://img.shields.io/badge/Field-Astroparticle%20Physics-green)

Este proyecto estudia la **radiación producida por rayos cósmicos en la atmósfera terrestre**, con especial enfoque en el flujo de **muones** y su contribución a la dosis de radiación a distintas altitudes.

El objetivo es combinar **modelos teóricos, simulaciones Monte Carlo y datos experimentales** para estimar cómo varía la radiación cósmica desde el nivel del mar hasta altitudes típicas de vuelo comercial.

---

# 🔬 Motivación científica

Los rayos cósmicos primarios (principalmente protones de alta energía) interactúan con la atmósfera terrestre produciendo **cascadas de partículas**.

Entre estas partículas destacan los **muones**, que pueden atravesar grandes espesores de materia y llegar hasta la superficie terrestre.

Comprender su flujo permite:

- estudiar la radiación atmosférica
- estimar dosis en aviación
- validar modelos de interacción hadrónica
- comparar simulaciones con detectores reales

---

# ⚙️ Metodología

El proyecto combina varias etapas.

## 1. Simulación de cascadas atmosféricas

Se utilizan simulaciones **Monte Carlo con CORSIKA** para modelar la interacción de rayos cósmicos con la atmósfera.

Configuración principal:

- Modelo hadrónico de alta energía: **SIBYLL 2.3e**
- Modelo de baja energía: **GHEISHA**
- Geometría atmosférica curva
- Producción explícita de muones

Las simulaciones generan archivos con las partículas secundarias detectadas.

---

## 2. Procesamiento de datos

Los resultados de las simulaciones se analizan usando herramientas en Python y ROOT para:

- identificar muones detectados
- calcular el flujo de partículas
- estudiar variaciones con la altitud

---

## 3. Conversión a dosis de radiación

A partir del flujo de muones se estima la **dosis equivalente de radiación** usando modelos simplificados de deposición de energía.

Se comparan dos aproximaciones:

**Modelo idealizado**

\[
D(h) = 0.0375 \cdot 2^{h/1500}
\]

**Modelo basado en simulación**

La dosis se calcula usando el flujo simulado de muones y su contribución relativa a la radiación total.

---

# 📊 Resultados esperados

El proyecto permite:

- estudiar cómo varía el flujo de muones con la altitud
- comparar modelos teóricos con simulaciones
- estimar dosis de radiación en vuelos comerciales
- validar simulaciones con datos experimentales

---

# 🧪 Aplicaciones

Este tipo de análisis es relevante en:

- **física de astropartículas**
- **radiación en aviación**
- **monitoreo atmosférico**
- **detectores de rayos cósmicos**

---

# 🚀 Trabajo futuro

- Comparación con datos experimentales usando detectores de centelleo
- Integración con **FLUKA** para cálculos de dosis más precisos
- Extensión del modelo a partículas adicionales (neutrones y electrones)

---

# 👨‍🔬 Autor

**Agustín Galdames Contreras**  
Licenciado en Física  
Universidad Andrés Bello
