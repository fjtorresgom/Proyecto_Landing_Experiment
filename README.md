# Proyecto 8 - Validación de Hipótesis de Negocio con Pruebas Estadísticas

## Descripción del proyecto

Este proyecto tiene como objetivo evaluar los resultados de un experimento A/B realizado sobre la página de inicio (landing page) de un ecommerce. Se compararon dos versiones de la página (A y B) para determinar cuál genera mejores resultados en términos de conversión y valor económico para el negocio.

A través de análisis exploratorio, pruebas estadísticas y visualizaciones, se busca responder preguntas clave para la toma de decisiones de marketing y optimización de la experiencia de usuario.

---

## Objetivos de negocio

Responder las siguientes preguntas:

- ¿Existe una diferencia significativa en el gasto promedio entre las versiones A y B?
- ¿Qué versión genera una mayor tasa de conversión?
- ¿La conversión depende de la fuente de tráfico?
- ¿El tipo de usuario influye en la conversión?
- ¿Qué recomendaciones pueden implementarse para optimizar la estrategia de marketing digital?

---

## Dataset utilizado

**Archivo:** `landing_experiment.csv`

Cada fila representa un usuario expuesto a una única versión de la landing page.

### Variables

| Variable | Descripción |
|-----------|-------------|
| user_id | Identificador único del usuario |
| date | Fecha de exposición al experimento |
| landing | Versión de la página (A o B) |
| region | Región geográfica del usuario |
| dispositivo | Tipo de dispositivo utilizado |
| traffic_source | Canal de adquisición |
| user_type | Tipo de usuario (Nuevo o Recurrente) |
| converted | Indicador de conversión (0 = No, 1 = Sí) |
| gasto | Valor monetario gastado por el usuario |

---

## Metodología

### 1. Carga y validación de datos

- Revisión de estructura del dataset.
- Verificación de valores nulos.
- Validación de usuarios únicos.
- Exploración de variables categóricas y numéricas.
- Verificación del balance del experimento A/B.

### 2. Comparación del gasto promedio

Se comparó el gasto promedio de los usuarios que realizaron una conversión utilizando una prueba t para muestras independientes.

**Hipótesis:**

- H₀: No existen diferencias en el gasto promedio entre las páginas A y B.
- H₁: Existen diferencias en el gasto promedio entre las páginas A y B.

### 3. Comparación de tasas de conversión

Se utilizó una prueba Z para comparar las tasas de conversión entre las páginas A y B.

**Hipótesis:**

- H₀: Las tasas de conversión son iguales.
- H₁: Las tasas de conversión son diferentes.

### 4. Relación entre fuente de tráfico y conversión

Se aplicó una prueba Chi-cuadrada de independencia para evaluar si la conversión depende del canal de adquisición.

### 5. Relación entre tipo de usuario y conversión

Se aplicó una prueba Chi-cuadrada de independencia para determinar si la conversión está asociada con el tipo de usuario.

### 6. Visualización de resultados

Se construyeron gráficos de:

- Cantidades absolutas de conversiones.
- Tasas de conversión por categoría.
- Comparaciones entre canales de tráfico.
- Comparaciones entre tipos de usuario.

---

## Principales hallazgos

### Landing Page

- La versión B presentó una tasa de conversión significativamente superior a la versión A.
- La versión B también mostró un gasto promedio significativamente mayor entre los usuarios convertidos.

### Fuente de tráfico

- Se encontró una asociación estadísticamente significativa entre la fuente de tráfico y la conversión.
- Organic fue el canal que generó el mayor volumen de conversiones.

### Tipo de usuario

- No se encontraron diferencias significativas entre usuarios nuevos y recurrentes respecto a la probabilidad de conversión.

---

## Recomendaciones

- Implementar la versión B de la landing page.
- Priorizar los canales de adquisición con mejor desempeño.
- Mantener estrategias similares para usuarios nuevos y recurrentes.
- Continuar realizando experimentos A/B para optimizar la experiencia del usuario y aumentar los ingresos.

---

## Herramientas utilizadas

- Python
- Pandas
- NumPy
- SciPy
- Statsmodels
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Cómo ejecutar el proyecto

### Opción 1: Google Colab

1. Descargar el notebook y el archivo `landing_experiment.csv`.
2. Abrir el notebook en Google Colab.
3. Cargar el dataset en el entorno de trabajo.
4. Ejecutar las celdas en orden.

### Opción 2: Jupyter Notebook

1. Clonar el repositorio.
2. Instalar las dependencias necesarias:

```bash
pip install pandas numpy scipy statsmodels matplotlib seaborn
```

3. Abrir el notebook:

```bash
jupyter notebook
```

4. Ejecutar todas las celdas en orden.

---

## Estructura del repositorio

```
├── README.md
├── Proyecto_8_AB_Testing.ipynb
├── datasets/
│   └── landing_experiment.csv
```

---

## Autor

**Francisco Javier Torres Gómez**

Proyecto desarrollado como parte del programa de formación en Data & Business Analytics de TripleTen.
