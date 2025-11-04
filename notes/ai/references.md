# Ruta de Estudio para la Creación de LLMs con Referencias de O'Reilly

A continuación, se detalla la ruta de estudio para el desarrollo de Large Language Models (LLMs), integrando los conceptos clave con bibliografía específica de la editorial O'Reilly (o disponible en su plataforma de aprendizaje).

---

## 1. Fundamentos de Matemáticas y Programación

**Descripción:** Dominio de Python y sus bibliotecas científicas (NumPy, PyTorch/TensorFlow). Requiere una base sólida en Álgebra Lineal (operaciones con matrices y tensores), Cálculo (derivadas, gradientes y _backpropagation_) y Estadística.

### 📚 Libros de O'Reilly Recomendados

- **Título:** _Python for Data Analysis, 3rd Edition_ por Wes McKinney.
  - **Enfoque:** Texto fundamental para el manejo de datos en Python. Cubre **NumPy** y **Pandas** a profundidad, prerrequisitos para manipular _datasets_ y tensores.
  - **Fuente:** <https://www.oreilly.com/library/view/python-for-data/9781098104023/>

- **Título:** _Fundamentals of Deep Learning, 2nd Edition_ por Nishant Buduma, et al.
  - **Enfoque:** Los capítulos iniciales (Cap. 1 y 2) cubren específicamente el **Álgebra Lineal** y la **Probabilidad** necesarias para entender el _deep learning_.
  - **Fuente:** <https://www.oreilly.com/library/view/fundamentals-of-deep/9781098132125/>

---

## 2. Aprendizaje Automático (Machine Learning) Clásico

**Descripción:** Comprensión de los conceptos básicos del ML: aprendizaje supervisado y no supervisado, regresión, clasificación, _overfitting_ y regularización.

### 📚 Libros de O'Reilly Recomendados

- **Título:** _Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow, 3rd Edition_ por Aurélien Géron.
  - **Enfoque:** La **Parte I** de este libro es una de las guías más reconocidas para el ML clásico. Cubre desde regresión lineal hasta SVMs y métodos _ensemble_ (Random Forests) usando **Scikit-Learn**.
  - **Fuente:** <https://www.oreilly.com/library/view/hands-on-machine-learning/9781098125967/>

---

## 3. Redes Neuronales Profundas (Deep Learning)

**Descripción:** Estudio de la arquitectura de redes neuronales (neuronas, capas, funciones de activación) y el proceso de entrenamiento (descenso de gradiente, _backpropagation_).

### 📚 Libros de O'Reilly Recomendados

- **Título:** _Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow, 3rd Edition_ por Aurélien Géron.
  - **Enfoque:** La **Parte II** del mismo libro es la continuación natural. Introduce redes neuronales, entrenamiento de redes profundas, CNNs y el uso de **TensorFlow/Keras**.
  - **Fuente:** <https://www.oreilly.com/library/view/hands-on-machine-learning/9781098125967/>

---

## 4. Procesamiento de Lenguaje Natural (NLP) Secuencial

**Descripción:** Comprensión de la tokenización, _embeddings_ (representaciones vectoriales como Word2Vec) y las arquitecturas secuenciales (Redes Neuronales Recurrentes - RNNs, LSTMs, GRUs).

### 📚 Libros de O'Reilly Recomendados

- **Título:** _Deep Learning for Natural Language Processing_ por Karthiek Reddy Bokka, et al.
  - **Enfoque:** Este libro (disponible en O'Reilly) se centra en los modelos de NLP pre-Transformers. Cubre explícitamente _embeddings_, **RNNs**, **LSTMs** y modelos _Sequence-to-Sequence_.
  - **Fuente:** <https://www.oreilly.com/library/view/deep-learning-for/9781484236857/>

---

## 5. Arquitectura Transformer

**Descripción:** Estudio profundo del artículo "Attention Is All You Need". Los conceptos clave son los mecanismos de **auto-atención** (_self-attention_) y _multi-head attention_, y las arquitecturas de _Encoder-Decoder_.

### 📚 Libros de O'Reilly Recomendados

- **Título:** _Natural Language Processing with Transformers, Revised Edition_ por Lewis Tunstall, Leandro von Werra, y Thomas Wolf.
  - **Enfoque:** Es el texto definitivo sobre el tema, escrito por ingenieros de Hugging Face. Se centra completamente en la arquitectura **Transformer** y cómo utilizar la biblioteca `transformers`.
  - **Fuente:** <https://www.oreilly.com/library/view/natural-language-processing/9781098136789/>

---

## 6. Técnicas de Entrenamiento y Ajuste Fino (Fine-Tuning)

**Descripción:** Comprender la diferencia entre el **pre-entrenamiento** (costoso, requiere clústeres de GPUs) y el **_fine-tuning_** (adaptación a tareas). Incluye técnicas de eficiencia (LoRA, QLoRA) y alineación (RLHF, DPO).

### 📚 Libros de O'Reilly Recomendados

- **Título:** _Fine-Tuning Large Language Models_ por Janakiram MSV.
  - **Enfoque:** Se enfoca en la adaptación de LLMs pre-entrenados. Cubre técnicas de _Parameter-Efficient Fine-Tuning_ (PEFT) como **LoRA**, cuantización (QLoRA) y el _fine-tuning_ de modelos _open-source_.
  - **Fuente:** <https://www.oreilly.com/library/view/fine-tuning-large-language/9781098157142/>

- **Título:** _Generative AI with Large Language Models_ (AWS/O'Reilly).
  - **Enfoque:** Proporciona una visión de alto nivel del ciclo de vida de los LLMs, incluyendo el pre-entrenamiento, el _fine-tuning_ y la alineación de modelos (como **RLHF**).
  - **Fuente:** <https://www.oreilly.com/library/view/generative-ai-with/9781098159290/>
