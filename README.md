# Evento Evaluativo 4 — Machine Learning

**Asignatura:** Análisis de Datos
**Carrera:** Ingeniería en Ciencia de Datos
**Departamento:** Sistemas
**Docente:** Daniel Alexis Nieto Mora
**Código del grupo:** 190304018-1
**Periodo:** 2026-2

---

## Equipo 1

| Integrante       |
|------------------|
| Diego Ramirez    |
| Liliana Arias    |
| Andres Botero    |
| Mateo Bolivar    |

---

## Descripción del evento

El Evento Evaluativo 4 tiene como objetivo aplicar los conocimientos adquiridos sobre **aprendizaje de máquina (Machine Learning)**. Cada equipo desarrolla modelos predictivos utilizando datasets reales, justificando las decisiones técnicas y evaluando el rendimiento con métricas apropiadas.

Según la asignación de ejercicios por grupo, a los **Equipos 1 y 8** les corresponden los **Ejercicios 1 y 5**.

---

## Ejercicios asignados

### Ejercicio 1 — Predicción del Rendimiento Académico

**Archivo:** `Ejercicio_1_Rendimiento_Academico.ipynb`
**Dataset:** `Ejercicio 1 student-mat.csv` (Student Grade Prediction Dataset)

**Problema:** Clasificación supervisada multiclase para estimar el nivel de rendimiento académico de estudiantes de matemáticas en tres categorías: **Bajo** (G3 < 10), **Medio** (10 ≤ G3 < 15) y **Alto** (G3 ≥ 15), a partir de variables como hábitos de estudio, relaciones familiares, consumo de alcohol y calificaciones anteriores.

**Modelos aplicados:**

| Modelo | Accuracy | F1-score |
|--------|----------|----------|
| Regresión Logística | 0.8608 | 0.8603 |
| SVM | 0.8228 | 0.8197 |
| KNN | 0.6582 | 0.6549 |

**Mejor modelo:** Regresión Logística — mayor Accuracy y F1-score.

**Contenido del notebook:**
1. Descripción del problema
2. Importación de librerías
3. Carga de datos
4. Exploración de datos (EDA): distribuciones, correlaciones, boxplots
5. Creación de variable objetivo (`Rendimiento`)
6. Preprocesamiento: imputación, estandarización, codificación (Pipeline)
7. Modelo 1 — Regresión Logística
8. Modelo 2 — KNN
9. Modelo 3 — SVM
10. Visualización PCA
11. Conclusiones e implicaciones éticas

---

### Ejercicio 5 — Predicción del Abandono de Empleados

**Archivo:** `Ejercicio_5_Abandono_Empleados.ipynb`
**Dataset:** `HR_comma_sep.csv` (HR Analytics Employee Attrition Dataset)

**Problema:** Clasificación supervisada binaria para identificar empleados con alta probabilidad de **abandonar la empresa** (`left = 1`) a partir de variables como nivel de satisfacción laboral, antigüedad, carga de trabajo, evaluaciones de desempeño y número de proyectos. El dataset contiene 14,999 registros con un desbalance de clases del ~24% (abandono).

**Modelos aplicados:**

| Modelo | Accuracy | F1-score | ROC-AUC |
|--------|----------|----------|---------|
| Regresión Logística | 0.7727 | 0.6277 | 0.8370 |
| Árbol de Decisión | 0.9397 | 0.8822 | 0.9595 |
| Random Forest | **0.9897** | **0.9779** | **0.9916** |

**Mejor modelo:** Random Forest — mejor desempeño en todas las métricas.

**Variables más importantes (Random Forest):**

| Variable | Importancia |
|----------|-------------|
| satisfaction_level | 0.272 |
| time_spend_company | 0.228 |
| average_montly_hours | 0.153 |
| number_project | 0.151 |
| last_evaluation | 0.138 |

**Contenido del notebook:**
1. Descripción del problema
2. Importación de librerías
3. Carga de datos
4. Exploración de datos (EDA): distribución de clases, análisis por departamento, salario, horas, antigüedad
5. Preprocesamiento: codificación, pipelines, split estratificado
6. Modelo 1 — Regresión Logística
7. Modelo 2 — Árbol de Decisión
8. Modelo 3 — Random Forest
9. Comparación de modelos
10. Curvas ROC-AUC
11. Importancia de variables
12. Visualización PCA
13. Conclusiones y acciones preventivas

---

## Estructura del repositorio

```
evaluacion 4/
├── README.md
├── Ejercicio_1_Rendimiento_Academico.ipynb
├── Ejercicio_5_Abandono_Empleados.ipynb
├── Ejercicio 1 student-mat.csv
└── HR_comma_sep.csv
```

---

## Requisitos

```
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

Instalación:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

---

## Criterios de evaluación cubiertos

- Comprensión del problema y análisis exploratorio de datos (EDA)
- Aplicación correcta y justificada de algoritmos de ML
- Calidad y claridad de las visualizaciones
- Evaluación y comparación de modelos con métricas adecuadas
- Interpretación de resultados y conclusiones fundamentadas
