# Primeros Pasos Keras: Tipos de Problemas Fundamentales

En este apartado se exploran los tres tipos de problemas más comunes en Machine Learning que sirven como introducción práctica al uso de redes neuronales con Keras:

1.  **Clasificación Binaria:** Predecir una de dos clases posibles (e.g., sí/no, 0/1).
2.  **Clasificación Multiclase:** Predecir una de *N* clases posibles (e.g., clasificar dígitos del 0 al 9).
3.  **Regresión:** Predecir un valor continuo (e.g., la tendencia de un precio).

Como ya se ha establecido, el entrenamiento de una red neuronal requiere de cuatro componentes clave:
- **Modelo:** Las capas encadenadas que transforman los datos.
- **Datos de Entrada y Objetivos (Target):** El conjunto de datos de entrenamiento y los resultados esperados.
- **Función de Pérdida (Loss Function):** La señal de retroalimentación utilizada para medir el error.
- **Optimizador:** El mecanismo que ajusta los pesos del modelo para minimizar la pérdida.

---

## Construcción de la Red: Capas y Unidades

### Arquitectura y Tipos de Capas

La construcción de la red neuronal depende de la estructura del tensor de entrada, el bloque principal es la **capa**.

| Tipo de Datos | Forma del Tensor | Capa Común | Descripción |
| :--- | :--- | :--- | :--- |
| **Vectoriales** | 2D: `(muestras, características)` | `Dense` | Capa completamente conectada. |
| **Secuenciales** | 3D: `(muestras, tiempo, características)` | `LSTM` | Capa Recurrente para secuencias. |
| **Imágenes** | 4D: `(muestras, alto, ancho, canales)` | `Conv2D` | Capa Convolucional. |

Los pesos de las capas son los **tensores aprendibles** que contienen el conocimiento de la red, y son ajustados mediante el descenso de gradiente estocástico.

### Unidades Ocultas (Dimensionalidad de la Representación)

El argumento clave en las capas **`Dense`** es el **número de unidades ocultas**.

* Este número define la **dimensión del espacio de representación** de la capa, es decir, cuánta **capacidad** (libertad para aprender) permitimos que tenga la red.
* Un número alto de unidades permite aprender representaciones más complejas, pero aumenta el riesgo de **sobreajuste (overfitting)** y el coste computacional.
* La arquitectura central consiste en elegir: cuántas capas encadenar y cuántas unidades ocultas asignar a cada una.

### 🧠 Función de Activación

Una capa **`Dense`** sin función de activación solo realizaría una transformación lineal: $\text{output} = (\mathbf{W} \cdot \mathbf{x} + \mathbf{b})$.

Para que la red pueda aprender transformaciones **no lineales** de los datos (lo cual es esencial para resolver problemas complejos), es necesario aplicar una **función de activación no lineal** después de la operación lineal.

* **`relu` (Unidad Lineal Rectificada):** Llama a cero los valores negativos. Es la activación por defecto en muchas capas ocultas.
* **`sigmoid` (Sigmoidea):** Comprime valores arbitrarios en el intervalo **$[0, 1]$**. Esto es útil para la capa de salida en problemas de clasificación binaria, donde los valores se interpretan como **probabilidades**.

---

## Configuración: Pérdida y Optimizador

### Función de Pérdida y Problemas

Para problemas de clasificación que arrojan resultados en forma de probabilidad, la función de pérdida más apropiada mide la distancia entre las distribuciones de probabilidad.

* **Clasificación Binaria:** La mejor opción es la **Entropía Cruzada Binaria (`binary\_crossentropy`)**. Esta métrica, proveniente de la Teoría de la Información, cuantifica la diferencia entre la distribución de probabilidad predicha por la red y la distribución de probabilidad verdadera (el objetivo).
* **Optimizador:** El optimizador (e.g., `RMSprop`, `Adam`) es el algoritmo que ajusta los pesos de la red basándose en la retroalimentación de la función de pérdida.