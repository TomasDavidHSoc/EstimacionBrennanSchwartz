# Estimación Bayesiana para el Modelo de Brennan-Schwartz

Este repositorio contiene la implementación y análisis de un modelo bayesiano para la calibración de tasas de interés de bonos gubernamentales (CETES y Bonos del Tesoro de EE.UU.). El proyecto se centra en la estimación de parámetros bajo el modelo de tasa de interés estocástica de **Brennan-Schwartz**, empleando métodos de simulación avanzada.

## 🚀 Metodología Técnica
El proyecto implementa un enfoque de inferencia bayesiana robusto:
1. **Modelado Estocástico**: Implementación de la dinámica de Brennan-Schwartz para la estructura temporal de las tasas de interés.
2. **Inferencia Bayesiana**: Implementación de algoritmos **MCMC (Markov Chain Monte Carlo)**, específicamente *Gibbs Sampler* y *Metropolis-within-Gibbs*, para la estimación de parámetros latentes.
3. **Simulación**: Validación mediante simulaciones **Monte Carlo** para evaluar la convergencia de las cadenas y la robustez de las estimaciones.
4. **Pruebas de Estrés**: Evaluación *Out-of-Sample* para medir la capacidad predictiva y el ajuste del modelo frente a la volatilidad de mercado.

## 📊 Fuentes de Datos
El modelo se alimenta de datos financieros obtenidos de fuentes oficiales mediante integración programática:
- **CETES (México):** Las series históricas de tasas de interés fueron obtenidas del **Portal de Datos Abiertos de Banxico**, garantizando la integridad de la información oficial.
- **TNX (Bonos del Tesoro EE.UU.):** La serie histórica fue consultada mediante la **API de `quantmod`** en R, permitiendo una actualización dinámica de las variables financieras.

## 📈 Resultados Clave
- Calibración exitosa de los parámetros de reversión a la media y volatilidad del modelo.
- Reconstrucción precisa de trayectorias estocásticas ajustadas a datos reales de mercado.
- Validación de convergencia mediante diagnósticos estadísticos de cadenas MCMC.

## 🛠 Tech Stack
- **Lenguaje**: R
- **Simulación y MCMC**: `Coda`, `mvtnorm`
- **Análisis de Datos**: `Tidyverse` (`dplyr`, `tidyr`), `Quantmod` (API de datos financieros)
- **Visualización**: `ggplot2`, `patchwork`, `MASS`

## 📂 Contenido del Repositorio
- `Estimacion_Bayesiana_para_el_Modelo_Brennan_Schwartz.ipynb`: Notebook detallado con el código fuente, lógica de estimación y resultados experimentales.
- `Estimación_Bayesiana_para_el_modelo_de_Brennan_Schwartz.pdf`: Reporte técnico formal con la deducción matemática del modelo, justificación bayesiana y análisis de resultados.
