# Guía Rápida de la API de Transformers

La API de Transformers permite trabajar fácilmente con modelos de procesamiento de lenguaje natural (NLP) como BERT, GPT y otros. Esta guía rápida te ayudará a comenzar.

## Objetivo

Utilizar modelos pre-entrenados para tareas como clasificación de texto, generación de texto, traducción y más.

## Preparación

- Python instalado
- Instalar la librería `transformers`:
    ```bash
    pip install transformers
    ```
- (Opcional) Instalar `torch` o `tensorflow` según el backend que prefieras.

## Cómo Usar

1. **Importar la librería:**
     ```python
     from transformers import pipeline
     ```
2. **Elegir una tarea y crear un pipeline:**
     ```python
     classifier = pipeline("sentiment-analysis")
     ```
3. **Realizar inferencias:**
     ```python
     result = classifier("Me encanta usar la API de Transformers.")
     print(result)
     ```

## Tareas Comunes

- **Clasificación de texto:** `pipeline("sentiment-analysis")`
- **Generación de texto:** `pipeline("text-generation")`
- **Traducción:** `pipeline("translation_en_to_es")`
- **Pregunta y respuesta:** `pipeline("question-answering")`

---

¡Explora el poder de los modelos de Transformers!

Para la guía completa de documentación, visita la [autenticacion](authentication.md).