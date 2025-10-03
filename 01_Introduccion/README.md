# 01 Introducción y Fundamentos

Este capítulo introduce las definiciones y las diferencias clave entre **Inteligencia Artificial (IA)**, **Machine Learning (ML)**, y **Deep Learning (DL)**, estableciendo el marco conceptual para el resto del libro.

---

## Conceptos Clave del Machine Learning

### 🎯 Machine Learning

El ML se centra en algoritmos que aprenden patrones a partir de datos, en lugar de ser programados explícitamente.

* **Entrada de datos:** Se proporcionan puntos de datos (imágenes, archivos, series de tiempo) junto con **ejemplos de resultados esperados** (etiquetas, transcripciones).
* **Función de Pérdida (Loss Function):** El mecanismo de medición que cuantifica la distancia entre las predicciones del modelo y los objetivos verdaderos. Actúa como la **señal de retroalimentación** fundamental para el proceso de aprendizaje.
* **Representación de Datos:** La forma en que se codifican los datos afecta directamente el rendimiento del modelo. Por ejemplo, para obtener tonos de color, el formato **RGB** puede ser mejor; para la saturación, el formato **HSV** puede simplificar el problema (cambio de coordenadas).

---

### 🧠 Deep Learning

El DL es una subdisciplina de ML que utiliza **Redes Neuronales Profundas** (con muchas capas).

* **Capas y Pesos:** El bloque de construcción principal es la **capa**, que implementa una transformación de datos definida por sus **pesos** o **parámetros**. El aprendizaje consiste en encontrar el conjunto óptimo de valores para estos pesos en cada capa.
* **Algoritmo Central:** La **Retropropagación (Backpropagation)** es el algoritmo que calcula el gradiente de la función de pérdida con respecto a los pesos. Esto permite al **Optimizador** ajustar los pesos en la dirección que minimiza la pérdida.
* **Bucle de Entrenamiento:** Los pesos iniciales son aleatorios. A través de este bucle iterativo, se ajustan progresivamente para acercarse al resultado deseado.

---

### 📊 Panorama de Algoritmos (Machine Learning Clásico)

El capítulo también hace mención a otros algoritmos de ML fuera del DL:

* **Modelos Probabilísticos:** Muchos modelos son estadísticos, como el clasificador **Naive Bayes** y la **regresión logística**, basados en el Teorema de Bayes.
* **Métodos Kernel:** Algoritmos como **SVM (Support Vector Machine)** buscan un hiperplano óptimo para la separación de clases. Son muy efectivos pero difíciles de escalar para grandes volúmenes de datos.
* **Árboles de Decisiones y Potenciación de Gradiente:**
    * **Random Forest** es considerado el segundo mejor algoritmo "generalista" para la mayoría de los problemas de ML clásico.
    * La **Potenciación de Gradiente (Gradient Boosting Machine)** es a menudo el mejor algoritmo para tratar **datos tabulares** o no perceptuales.
* **Redes Neuronales Convolucionales (ConvNets):** Son el algoritmo de referencia en tareas de **visión por ordenador** (ej. ImageNet para clasificación de imágenes de alta resolución).

---

## 💻 Conceptos Técnicos de la Red Neuronal

### Flujo de Trabajo

El flujo de trabajo estándar de una red neuronal es:
1.  Proporcionar los datos de entrenamiento.
2.  La red aprende la asociación entre los datos y las etiquetas.
3.  Se solicitan **predicciones** para datos de prueba (`test_images`), y se comprueba su precisión contra las etiquetas de prueba (`test_labels`).

### Bloque de Construcción: La Capa

El Deep Learning es un proceso de **destilación o filtrado** que encadena capas. Cada capa refina los datos, extrayendo representaciones cada vez más complejas y significativas.

### ⚙️ Proceso de Compilación

Para configurar la red antes del entrenamiento, se necesitan tres elementos clave:

1.  **Función de Pérdida (Loss Function):** Mide la precisión de la red y el rendimiento.
2.  **Optimizador:** El mecanismo que implementa la retropropagación para actualizar los pesos de la red.
3.  **Métricas:** Valores a monitorear durante el entrenamiento y la prueba (e.g., la **precisión/accuracy** media).

### 🔢 Representación de Datos: Tensores

La estructura de datos fundamental en Machine Learning es el **tensor**, un contenedor para datos almacenados en matrices NumPy multidimensionales.

| Rango | Nombre | Descripción | Uso Común |
| :---: | :---: | :--- | :--- |
| **0D** | Escalar | Un solo número. | Temperatura, edad. |
| **1D** | Vector | Una cadena de números. | Series de tiempo, características. |
| **2D** | Matriz | Una cadena de vectores (filas y columnas). | Datos tabulares: `(muestras, características)`. |
| **3D** | Tensor 3D | Una cadena de matrices. | Datos secuenciales: `(muestras, tiempo, características)`. |
| **4D** | Tensor 4D | Imágenes. | `(muestras, altura, anchura, canales)`. |
| **5D** | Tensor 5D | Video. | `(muestras, fotograma, altura, anchura, canales)`. |

* **Atributos Clave:**
    * `x.ndim`: El **rango** (número de ejes o dimensiones).
    * `shape`: La forma del tensor, una tupla que indica el tamaño de cada eje (e.g., `(60000, 28, 28)`).
    * `dtype`: El tipo de datos que contiene el tensor (ej. `float32`).

### Lotes de Datos

En Deep Learning, los datos se procesan en **lotes (batches)** pequeños (subconjuntos `x.[a:b]`) en lugar de alimentar la red con todo el conjunto de datos a la vez. El **eje 0** del tensor siempre corresponde al **eje de la muestra** o dimensión del lote.
