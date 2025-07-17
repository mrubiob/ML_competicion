# Análisis de Personalidad con Machine Learning

## Descripción del Proyecto

Este proyecto implementa un sistema de clasificación de personalidad utilizando técnicas de Machine Learning para predecir si una persona es **Extrovertida** o **Introvertida** basándose en patrones de comportamiento social.

## Objetivo

Desarrollar un modelo predictivo que pueda clasificar automáticamente el tipo de personalidad de individuos utilizando características comportamentales, con el fin de alcanzar una precisión superior al 90%.

## Dataset

### Información General
- **Registros**: 2,900 entradas
- **Características**: 8 variables (5 numéricas, 3 categóricas)
- **Distribución**: 
  - Extrovertidos: 1,491 (51.4%)
  - Introvertidos: 1,409 (48.6%)
- **Balance**: Dataset naturalmente balanceado

### Variables del Dataset

| Variable | Tipo | Descripción |
|----------|------|-------------|
| `Time_spent_Alone` | Numérica | Tiempo que pasa solo (0-11) |
| `Stage_fear` | Categórica | Miedo escénico (Yes/No) |
| `Social_event_attendance` | Numérica | Asistencia a eventos sociales (0-10) |
| `Going_outside` | Numérica | Frecuencia de salidas (0-7) |
| `Drained_after_socializing` | Categórica | Agotamiento post-social (Yes/No) |
| `Friends_circle_size` | Numérica | Tamaño del círculo de amigos (0-15) |
| `Post_frequency` | Numérica | Frecuencia de publicaciones (0-10) |
| `Personality` | Categórica | **Variable objetivo** (Extrovert/Introvert) |

##  Preprocesamiento de Datos

### Limpieza de Datos
- **Duplicados eliminados**: 731 registros duplicados removidos
- **Valores faltantes**: Dataset completo sin valores nulos
- **Outliers identificados**: Mantenidos por su valor interpretativo



##  Modelos Implementados

### Comparación de Algoritmos

| Modelo | Accuracy | Ranking |
|--------|----------|---------|
| **SVM** | **90.8%** | 🥇 |
| **Regresión Logística** | 90.6% | 🥈 |
| **KNN** | 90.4% | 🥉 |
| **Árbol de Decisión** | 89.4% | 4° |
| **Random Forest** | 87.8% | 5° |


##  Instalación y Uso

### Requisitos
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Resultados y Métricas

### Métricas de Evaluación
- **Accuracy**: 90.8%


### Matriz de Confusión
```
                Predicción
Actual    Extrovert  Introvert
Extrovert    [TP]      [FN]
Introvert    [FP]      [TN]
```

### Insights Principales

1. **Variables más predictivas**:
   - `Time_spent_Alone`: Fuerte indicador de introversión
   - `Social_event_attendance`: Correlaciona con extroversión
   - `Drained_after_socializing`: Discriminador clave

2. **Patrones identificados**:
   - Extrovertidos: Mayor actividad social, círculos amplios
   - Introvertidos: Más tiempo solo, menor frecuencia social

##  Análisis de Outliers

### Outliers Identificados
- `Time_spent_Alone`: Valores extremos (11.0 vs Q3: 7.0)
- `Friends_circle_size`: Círculos excepcionalmente grandes (15.0 vs Q3: 10.0)
- `Social_event_attendance`: Hiperactividad social (10.0 vs Q3: 7.0)

### Decisión: **Mantener outliers**
- Representan comportamientos legítimos extremos
- Valiosos para la diversidad del modelo
- Contribuyen a la robustez predictiva

## Optimización del Modelo

### Técnicas Aplicadas

1. **GridSearchCV**: Búsqueda exhaustiva de hiperparámetros



## Metodología

### Pipeline de Machine Learning

1. **Exploración de Datos** (EDA)
2. **Preprocesamiento** y limpieza
3. **Ingeniería de características**
4. **Selección de modelos**
5. **Optimización de hiperparámetros**
6. **Evaluación y validación**
7. **Interpretación de resultados**

### Validación del Modelo


- **Métricas múltiples**: Accuracy, Precision, Recall, F1


## Conclusiones

### Hallazgos Principales

1. **Alta predictibilidad**: Los patrones de comportamiento social son altamente predictivos de la personalidad
2. **Dataset de calidad**: Balance natural y características relevantes
3. **SVM superior**: Mejor performance para este tipo de datos
4. **Interpretabilidad**: Variables claras y significativas







##  Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

