# TFG — Machine Learning para identificar la vía ALT en datos genómicos tumorales

Trabajo de Fin de Grado (Ingeniería en Sistemas de Información, Universidad de Alcalá). Análisis con Machine Learning para predecir la actividad de la vía **ALT** (*Alternative Lengthening of Telomeres*) a partir de datos clínicos y genómicos de pacientes con cáncer, usando la **tasa de fusiones teloméricas** como variable objetivo.

## Objetivo

Determinar qué variables —tipo de tumor, mutaciones en genes *driver* y tratamientos recibidos— se asocian con la actividad ALT, y comparar distintos modelos de regresión para predecirla tanto en tumor como en sangre periférica.

## Metodología

| Fase | Notebook | Contenido |
|---|---|---|
| Exploración | `01_EDA.ipynb` | Análisis exploratorio, nulos, distribución del target |
| Limpieza | `02_limpieza.ipynb` | Depuración, codificación de variables y construcción del dataset |
| Modelos lineales | `03a`, `03c` | Lasso, Ridge y Elastic Net (features verdes y azules) |
| Modelos no lineales | `03b`, `03d` | Random Forest, XGBoost y LightGBM |
| Tipo de tumor + mutaciones | `03e`, `03g` | Modelos con genes driver (target tumor y sangre) |
| Modelo combinado | `03f` | Tipo de tumor + mutaciones + tratamientos |
| Tratamientos (sangre) | `03h` | Modelos lineales con target en sangre |
| Modelos avanzados | `03i` | Hurdle model y TabPFN |
| Optimización | `03j` | Búsqueda de hiperparámetros con Optuna |
| Interpretabilidad | `03k` | SHAP values (importancia y dirección de cada variable) |
| Mutaciones | `04_mutaciones.ipynb` | Ranking de genes por tasa de fusiones (ATRX, DAXX, …) |

## Tecnologías

Python · pandas · scikit-learn · XGBoost · LightGBM · Optuna · SHAP · TabPFN · matplotlib · seaborn

## Nota sobre los datos

Los datos clínicos y genómicos utilizados son de **acceso controlado** (Hartwig Medical Foundation / ICGC) y **no se incluyen** en este repositorio. Los notebooks muestran el código y los resultados agregados del análisis, sin datos de pacientes individuales.

---
Autor: **Pablo Esquinas Cordero** · [LinkedIn](https://www.linkedin.com/in/pablo-esquinas-cordero)
