# Generación de Texto Jurídico con GPT-2

### Fine-Tuning de Modelos Generativos en Español para Dominio Legal

<p align="center">
  <img src="https://img.shields.io/badge/Estado-Finalizado-success?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/NLP-Generativo-blueviolet?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Modelo-GPT--2-black?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Framework-HuggingFace-yellow?style=for-the-badge&logo=huggingface"/>
  <img src="https://img.shields.io/badge/Backend-PyTorch-red?style=for-the-badge&logo=pytorch"/>
</p>

<p align="center">
  <b>Mini-Proyecto – Procesamiento de Lenguaje Natural</b><br>
  Maestría en Inteligencia Artificial Aplicada – Universidad ICESI<br>
  <i>Profesor: Luis Eduardo Ferro Diez</i>
</p>

---

## 1. Planteamiento del Problema

El dominio jurídico se caracteriza por el uso de lenguaje altamente estructurado, formal y especializado. Sin embargo, la generación automática de este tipo de contenido en español sigue siendo un desafío debido a:

* Escasez de datasets jurídicos bien estructurados
* Complejidad semántica del lenguaje legal
* Limitaciones de modelos preentrenados generalistas

**Problema:**

> ¿Cómo adaptar un modelo generativo preentrenado para producir texto jurídico coherente y contextualizado en español?

---

## 2. Objetivos

### 🔹 Objetivo General

Desarrollar un modelo generativo basado en GPT-2 capaz de producir texto jurídico en español mediante fine-tuning.

### 🔹 Objetivos Específicos

* Implementar un pipeline completo de NLP generativo
* Adaptar GPT-2 al dominio jurídico
* Evaluar cualitativamente la generación de texto
* Comparar estrategias de generación

---

## 3. Metodología

Se sigue un enfoque estructurado alineado con buenas prácticas en PLN:

### 🔹 Fases del proceso

```mermaid id="f3z6e1"
flowchart LR
A[Dataset Jurídico] --> B[Preprocesamiento]
B --> C[Tokenización]
C --> D[Modelo GPT-2]
D --> E[Fine-Tuning]
E --> F[Generación]
F --> G[Evaluación]
```

### 🔹 Descripción técnica

| Fase             | Descripción                        |
| ---------------- | ---------------------------------- |
| Preprocesamiento | Limpieza y normalización del texto |
| Tokenización     | Uso de tokenizer de GPT-2          |
| Entrenamiento    | Ajuste fino del modelo             |
| Generación       | Sampling controlado                |
| Evaluación       | Análisis cualitativo               |

---

## 4. Estructura del Proyecto

```id="estructura-proyecto"
📦 mini-proyecto-gpt-juridico
 ┣ 📜 notebook_colab.ipynb
 ┣ 📜 README.md
 ┣ 📜 requirements.txt
 ┗ 📂 data/
     ┗ 📄 dataset_juridico.txt
```

## 5. Implementación Técnica

### 🔹 Modelo utilizado

* GPT-2 (preentrenado)
* Fine-tuning con dataset jurídico

### 🔹 Librerías

* Transformers
* PyTorch
* Datasets

---

## 6. Estrategias de Generación

### 🔹 Método 1: Generación personalizada

Permite control detallado de:

* Temperatura
* Longitud
* Probabilidad acumulada

### 🔹 Método 2: Generación estándar

```python id="codigo-generacion"
model.generate(
    input_ids,
    max_length=150,
    temperature=0.7,
    top_k=50,
    top_p=0.95
)
```

 **Justificación técnica:**
El uso de `top_k` y `top_p` permite balancear entre diversidad y coherencia del texto generado.

---

## 7. Resultados y Análisis

### 🔹 Resultados observados

* Generación coherente en contexto jurídico
* Uso adecuado de conectores legales
* Estructura formal consistente

### 🔹 Ejemplo generado

> “El contrato de arrendamiento establece que las partes deberán cumplir con las obligaciones pactadas conforme a la normatividad vigente...”

---

## 8. Discusión

Los resultados evidencian que:

* El **fine-tuning mejora significativamente la especialización del modelo**
* GPT-2, aunque generalista, puede adaptarse a dominios específicos
* La calidad depende fuertemente del dataset

Sin embargo:

* No garantiza validez jurídica real
* Puede generar ambigüedades semánticas
* Carece de razonamiento legal profundo

---

## 9. Limitaciones

* Dataset limitado
* Evaluación solo cualitativa
* No se mide perplexity ni BLEU
* Riesgo de overfitting

---

## 10. Trabajo Futuro

* Implementar LLaMA o GPT-Neo
* Incorporar evaluación cuantitativa
* Aumentar dataset jurídico
* Integración con sistemas legales

---

## 🔁 11. Reproducibilidad

### 🔹 Instalación

```bash
pip install -r requirements.txt
```

### 🔹 Ejecución

* Abrir en Google Colab
* Ejecutar todas las celdas

Se recomienda GPU

---

## 12. Autores

* Juan Manuel Hurtado Angulo
* Manuel Alberto González González
* William Alberto Reina García

---

## 13. Referencias

* Radford et al. (2019). *Language Models are Unsupervised Multitask Learners*
* Vaswani et al. (2017). *Attention is All You Need*
* Documentación de Hugging Face

---

## 14. Conclusión

Este proyecto demuestra que los modelos generativos pueden ser adaptados a dominios especializados como el jurídico, evidenciando el potencial de la IA generativa en contextos profesionales.
o dime: **“vamos a sustentación”**

