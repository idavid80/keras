# Deep Learning con Keras: Prácticas del libro "Deep Learning with Python" 🧠

Este repositorio alberga las implementaciones, ejercicios y proyectos de código que realicé mientras estudiaba la **Primera Edición** del libro **"Deep Learning with Python"** de **François Chollet**.

El objetivo es tener un lugar centralizado y funcional para practicar y dominar los conceptos fundamentales del Deep Learning usando **Python** y la librería **Keras/TensorFlow**.

---

## 🚀 Cómo Usar Este Repositorio

Todos los ejercicios están implementados como *Jupyter Notebooks* (`.ipynb`), diseñados para ejecutarse sin problemas en **Google Colab**.

Para empezar a practicar:

1.  **Clonar o Descargar** este repositorio.
2.  Abrir Google Colab.
3.  Hacer clic en `Archivo > Abrir Notebook`.
4.  Seleccionar la pestaña **GitHub** o **Subir** y cargar el archivo `.ipynb` deseado.

> **Nota:** Todos los datos (datasets) necesarios para los ejercicios se cargan directamente dentro de los notebooks desde **Keras** o **TensorFlow**, siguiendo el espíritu del libro.

---

## ⚙️ Nota Importante sobre la Versión (TensorFlow 2.x)

El libro original fue publicado en 2017, coincidiendo con una versión anterior de Keras (Keras 1.x o standalone).

Por ello, **todo el código ha sido actualizado** para ser completamente compatible con la API **`tf.keras`** integrada en **TensorFlow 2.x**. Si encuentras sintaxis o funciones que difieren del código impreso en la primera edición, esta actualización es la razón.

⚠️ Tenga en cuenta que, debido a la rápida evolución del campo, algunas implementaciones pueden seguir cambiando. Siempre se recomienda consultar la [Segunda Edición del libro (2021)](https://www.manning.com/books/deep-learning-with-python-second-edition) para el código más reciente.

---

## 📂 Estructura del Contenido (Organizado por Capítulos)

El código está organizado de manera que facilita el seguimiento del libro, con un *Jupyter Notebook* por sección o tema principal de cada capítulo:

```plaintext
├── 01_Introduccion/                  # Fundamentos de IA, ML, y DL
├── 02_Bloques_Matematicos/           # Introducción a los tensores y la Retropropagación
├── 03_Primeros_Pasos_Keras/          # Clasificación binaria, multiclase y regresión
├── 04_Fundamentos_ML/                # Overfitting, Underfitting, Regularización y Validación
├── 05_Vision_Artificial_ConvNets/    # Redes Convolucionales (ConvNets) para imágenes
├── 06_Secuencias_y_Texto_RNN/        # Procesamiento de texto, Embeddings y Redes Recurrentes (RNNs)
├── 07_Mejores_Practicas_Avanzadas/   # Más allá del entrenamiento básico
├── 08_Deep_Learning_Generativo/      # VAEs, GANs y modelos generativos
└── ...
```
| Capítulo | Descripción | Notebooks (Abrir y Ejecutar) |
| :--- | :--- | :--- |
| **01** | Introducción a IA, ML, y DL | [01_Introduccion.ipynb] [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/idavid80/keras/blob/main/01_Introduccion/01_Introduccion.ipynb) |
| **02** | Bloques Matemáticos | [02_Bloques_Matematicos.ipynb] [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/idavid80/keras/blob/main/02_Bloques_Matematicos/02_Bloques_Matematicos.ipynb) |
| ... | ... | ... |

---

## 📚 Sobre el Libro

**Título:** Deep Learning with Python

**Autor:** [François Chollet](https://fchollet.com/)

**Edición:** [Primera Edición (2017)]((https://www.manning.com/books/deep-learning-with-python))

**Editorial:** Manning Publications

**Enlace Oficial:** [Segunda edición](https://www.manning.com/books/deep-learning-with-python-second-edition?a_aid=keras&a_bid=76564dff)

---

🤝 Contribuciones y Debugging

Si encuentras algún error en las implementaciones actualizadas o tienes sugerencias para mejorar el código, no dudes en abrir un issue o enviar un Pull Request.

Adoptando el espíritu del Pato de Goma 🐍 (un concepto clave en El Programador Pragmático), te animamos a probar una técnica de depuración antes de reportar un bug:

Explícale el código a tu Pato de Goma imaginario (o real), línea por línea.

Si al explicarlo en voz alta descubres el fallo, ¡felicidades!

Si después de la explicación el pato sigue confundido, ¡entonces es un bug real! Abre un issue y juntos lo resolveremos.

¡El aprendizaje es mejor en comunidad!
