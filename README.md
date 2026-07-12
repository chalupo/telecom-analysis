# 📊 Análisis de Clientes y Uso de Servicios Móviles - ConnectaTel

## 📖 Descripción del proyecto

Este proyecto consiste en un análisis exploratorio y estadístico del comportamiento de los clientes de **ConnectaTel**, una empresa de telecomunicaciones con operaciones en Latinoamérica.

El objetivo es comprender cómo utilizan los clientes los servicios móviles (llamadas y mensajes), identificar patrones de consumo, detectar valores atípicos y construir segmentos de usuarios que permitan generar recomendaciones comerciales para optimizar la oferta de planes y mejorar la experiencia del cliente.

Todo el análisis fue desarrollado en Python utilizando un Jupyter Notebook, siguiendo un proceso de limpieza, exploración, visualización y segmentación de datos.

---

# 🎯 Objetivo

Analizar el comportamiento de los clientes de ConnectaTel mediante técnicas de análisis exploratorio de datos (EDA) para responder las siguientes preguntas de negocio:

- ¿Qué segmentos de clientes presentan mayor o menor uso de llamadas y mensajes?
- ¿Existen usuarios con comportamientos atípicos?
- ¿Cómo varía el consumo según la edad y el plan contratado?
- ¿Qué oportunidades comerciales pueden identificarse a partir de los patrones encontrados?

---

# 📂 Datasets utilizados

El proyecto utiliza tres conjuntos de datos:

### plans.csv

Información de los planes disponibles.

Incluye variables como:

- Nombre del plan
- Precio mensual
- Minutos incluidos
- GB incluidos
- Precio por minuto adicional
- Precio por GB adicional
- Precio por mensaje adicional

---

### users_latam.csv

Información de los clientes.

Incluye:

- ID del usuario
- Nombre
- Edad
- Ciudad
- Fecha de registro
- Plan contratado
- Fecha de baja (churn)

---

### usage.csv

Registro histórico del uso de los servicios.

Incluye:

- Usuario
- Tipo de actividad (llamada o mensaje)
- Fecha
- Duración de llamada
- Longitud del mensaje

---

# 🛠 Tecnologías utilizadas

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

# 📈 Etapas del análisis

El proyecto fue desarrollado siguiendo el siguiente flujo de trabajo:

## 1. Carga y exploración de datos

- Carga de los tres datasets.
- Revisión de estructura.
- Inspección de tipos de datos.
- Exploración inicial de columnas.

---

## 2. Identificación de problemas de calidad

Se revisaron:

- Valores nulos
- Valores inválidos (sentinels)
- Fechas fuera de rango
- Distribuciones iniciales
- Tipos de datos

---

## 3. Limpieza de datos

Se realizaron las siguientes acciones:

- Reemplazo del sentinel **-999** en edad por la mediana.
- Conversión de fechas al formato datetime.
- Reemplazo del valor inválido **"?"** en ciudad por valores nulos.
- Marcado de fechas futuras como valores nulos.
- Validación de valores faltantes en llamadas y mensajes.

---

## 4. Construcción del perfil del usuario

Se agregaron métricas de uso por usuario:

- Cantidad de mensajes
- Cantidad de llamadas
- Total de minutos de llamadas

Posteriormente se integraron con la información de usuarios.

---

## 5. Análisis estadístico

Se calcularon estadísticas descriptivas para:

- Edad
- Cantidad de mensajes
- Cantidad de llamadas
- Minutos de llamadas

También se analizó la distribución de los planes contratados.

---

## 6. Visualización

Se construyeron:

- Histogramas
- Boxplots

Para identificar:

- Distribuciones
- Asimetrías
- Valores atípicos

---

## 7. Detección de outliers

Se utilizó el método del **Rango Intercuartílico (IQR)** para detectar valores extremos.

Los outliers encontrados fueron conservados debido a que representan comportamientos reales de consumo y aportan información relevante para el negocio.

---

## 8. Segmentación de clientes

Se generaron dos segmentaciones:

### Segmentación por nivel de uso

- Bajo uso
- Uso medio
- Alto uso

### Segmentación por edad

- Joven
- Adulto
- Adulto Mayor

---

## 9. Insights ejecutivos

Finalmente se elaboraron conclusiones y recomendaciones para apoyar la toma de decisiones del negocio.

---

# ▶️ Cómo ejecutar el proyecto

## Opción 1: Google Colab

1. Descarga este repositorio.
2. Abre Google Colab.
3. Selecciona **Archivo → Subir notebook**.
4. Carga el archivo `.ipynb`.
5. Sube también los archivos:

- plans.csv
- users_latam.csv
- usage.csv

6. Ajusta las rutas de lectura si es necesario.
7. Ejecuta todas las celdas desde el menú:

**Entorno de ejecución → Ejecutar todo**

---

## Opción 2: Jupyter Notebook

1. Clona o descarga este repositorio.
2. Instala las dependencias necesarias.
3. Coloca los tres archivos CSV dentro de la carpeta `/datasets`.
4. Abre el notebook.
5. Ejecuta todas las celdas en orden.

---

# 📦 Dependencias

Instalar con:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

---

# 📁 Estructura esperada del proyecto

```
Proyecto_ConnectaTel/
│
├── README.md
├── Analisis_ConnectaTel.ipynb
│
└── datasets/
    ├── plans.csv
    ├── users_latam.csv
    └── usage.csv
```

---

# 🔄 Guía de reproducción

Para reproducir completamente el análisis:

1. Descargar el proyecto.
2. Instalar las dependencias.
3. Colocar los datasets en la carpeta `/datasets`.
4. Abrir el notebook.
5. Ejecutar todas las celdas en el orden establecido.
6. Revisar las visualizaciones, estadísticas e insights generados automáticamente.

El notebook es completamente reproducible siempre que se mantenga la misma estructura de carpetas y los mismos archivos de entrada.

---

# 📌 Resultados principales

Durante el análisis se identificó que:

- Fue necesario corregir valores inválidos y fechas fuera de rango.
- Los usuarios presentan comportamientos de uso similares entre los planes Básico y Premium.
- Existen usuarios con consumos significativamente superiores al promedio, considerados outliers, pero representativos del comportamiento real.
- La segmentación por nivel de uso permite identificar oportunidades para personalizar ofertas comerciales y estrategias de fidelización.

---

# 👤 Autor

Proyecto desarrollado como práctica de Análisis Exploratorio de Datos (EDA) utilizando Python y Jupyter Notebook.
