# 📈 Curso de Series de Tiempo con R

[![R](https://img.shields.io/badge/R-%23276DC3.svg?style=flat&logo=r&logoColor=white)](https://www.r-project.org/)
[![Estado](https://img.shields.io/badge/Estado-Activo-success)]()
[![Licencia](https://img.shields.io/badge/Licencia-MIT-blue.svg)](LICENSE)

¡Bienvenido al repositorio oficial del **Curso de Análisis y Predicción de Series de Tiempo utilizando R**! Este espacio ha sido diseñado para recopilar todo el material teórico-práctico, scripts automatizados, conjuntos de datos reales y guías metodológicas necesarias para dominar el modelado de datos secuenciales y cronológicos.

---

## 📑 Tabla de Contenidos
1. [Descripción del Curso](#-descripción-del-curso)
2. [Objetivos de Aprendizaje](#-objetivos-de-aprendizaje)
3. [Requisitos Previos](#-requisitos-previos)
4. [Instalación y Configuración](#-instalación-y-configuración)
5. [Estructura del Repositorio](#-estructura-del-repositorio)
6. [Librerías Clave Utilizadas](#-librerías-clave-utilizadas)
7. [Contribución](#-contribución)
8. [Autor](#-autor)

---

## 📖 Descripción del Curso
El análisis de series de tiempo es una disciplina estadística fundamental para comprender comportamientos históricos y proyectar tendencias futuras en áreas como las finanzas, la economía, la meteorología y las operaciones empresariales. 

A través de este curso, aprenderás a identificar los componentes clave de una serie (tendencia, estacionalidad, ciclos e irregularidades), validar supuestos estadísticos críticos (como la estacionariedad y la autocorrelación), y desplegar modelos robustos de pronóstico que asistan en la toma de decisiones estratégicas.

---

## 🎯 Objetivos de Aprendizaje
* **Manipular y estructurar** datos temporales de manera eficiente utilizando el ecosistema de R.
* **Descomponer series temporales** para aislar patrones subyacentes e interpretar gráficos de autocorrelación (ACF) y autocorrelación parcial (PACF).
* **Implementar métodos de suavizado** exponencial tradicional (Holt-Winters) para pronósticos de corto y mediano plazo.
* **Construir, validar y optimizar** modelos predictivos avanzados de la familia ARIMA y SARIMA.
* **Evaluar la precisión** de los modelos implementando métricas de error estándar (ME, RMSE, MAE, MPE, MAPE, MASE).

---

## 🛠 Requisitos Previos
Para garantizar un flujo de trabajo óptimo, asegúrate de cumplir con los siguientes prerrequisitos en tu entorno local:
* Conocimientos fundamentales de estadística descriptiva e inferencial.
* Familiaridad básica con la sintaxis de R (vectores, data frames, funciones).
* Tener instaladas las versiones más recientes de:
  * [R Project (v4.2+)](https://cran.r-project.org/)
  * [RStudio Desktop](https://posit.co/download/rstudio-desktop/)

---

## 💻 Instalación y Configuración

Sigue estos pasos para clonar el proyecto y preparar tu entorno local:

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/emanuelmejia/course_time_series_r.git
   cd course_time_series_r
   ```

2. **Configurar el entorno en R:**
   Abre RStudio y ejecuta el siguiente bloque de código para instalar de manera automática todas las dependencias requeridas para el desarrollo de las prácticas:
   ```R
   # Lista de paquetes necesarios
   paquetes <- c("tidyverse", "lubridate", "forecast", "tseries", 
                 "astsa", "ggplot2", "timetk", "fable", "feasts")

   # Instalación automatizada
   paquetes_nuevos <- paquetes[!(paquetes %in% installed.packages()[,"Package"])]
   if(length(paquetes_nuevos)) install.packages(paquetes_nuevos)
   
   print("¡Configuración completada con éxito!")
   ```

---

## 🗂 Estructura del Repositorio

El contenido está estructurado de forma modular para facilitar el aprendizaje:

```text
course_time_series_r/
│
├── data/                      # Conjuntos de datos reales (.csv, .rds)
│   ├── ventas_mensuales.csv
│   └── demanda_electrica.rds
│
├── 01_Introduccion/           # Manipulación de fechas con lubridate y objetos ts
│   ├── 01_fechas_y_objetos_ts.R
│   └── Tarea_1_Introduccion.R
│
├── 02_Analisis_Exploratorio/  # Descomposición, estacionariedad y funciones de autocorrelación
│   ├── 02_descomposicion_y_acf.R
│   └── 02_pruebas_estacionariedad.R
│
├── 03_Suavizado_Exponencial/  # Modelos de Holt, Holt-Winters y suavizado simple
│   └── 03_metodos_suavizado.R
│
├── 04_Modelos_ARIMA/          # Identificación, estimación y diagnóstico SARIMA
│   ├── 04_modelado_arima.R
│   └── 04_diagnostico_residuos.R
│
├── scripts/                   # Funciones personalizadas y utilidades globales
│   └── graficos_auxiliares.R
│
└── README.md                  # Archivo de presentación (este archivo)
```

---

## 📦 Librerías Clave Utilizadas

* **`tidyverse` & `lubridate`**: Para la limpieza de datos y manipulación quirúrgica de fechas y horas.
* **`forecast`**: La librería clásica por excelencia para modelado y predicción automática (funciones `auto.arima`, `ets`).
* **`tseries`**: Esencial para pruebas de hipótesis estadísticas como la prueba de Dickey-Fuller Aumentada (ADF).
* **`fable` & `feasts`**: Herramientas de última generación pertenecientes al ecosistema *tidyverts* para modelado y análisis moderno de series de tiempo.

---

## 🤝 Contribución

Las contribuciones hacen que la comunidad de código abierto sea un lugar increíble para aprender, inspirar y crear. Cualquier contribución que hagas será **muy valorada**.

1. Haz un Fork del proyecto.
2. Crea una rama para tu característica o corrección (`git checkout -b feature/NuevaMejora`).
3. Confirma tus cambios (`git commit -m 'Añade una nueva mejora funcional'`).
4. Sube la rama (`git push origin feature/NuevaMejora`).
5. Abre un *Pull Request*.

---

## 👤 Autor

**Emanuel Mejia**
* **GitHub**: [@emanuelmejia](https://github.com/emanuelmejia)
* **LinkedIn**: [Emanuel Mejía](https://www.linkedin.com/in/emanuel-mejia-firedrop)

---
*Este repositorio fue creado con fines educativos. Si el contenido te resulta útil, ¡no olvides darle una ⭐!*