# ICC: Human vs. LLM Spanish Academic Texts

Este repositorio acompaña el artículo:

> *Comparación de patrones léxicos, sintácticos y de coherencia macroestructural en textos académicos en español: escritura humana vs. generada por LLM*  
> Diana Kristhi — Maestría en Lingüística, 2026

## Descripción

Corpus y código de análisis lingüístico comparativo entre textos académicos en español escritos por humanos y generados por herramientas de IA generativa basadas en LLM (ChatGPT, Copilot). El estudio analiza tres niveles de descripción lingüística: léxico-semántico, sintáctico y coherencia macroestructural.

## Estructura del repositorio

```
├── prompt/
│   └── prompt_generacion.md           # Prompt completo usado para generar los corpus
├── scripts/
│   ├── analisis_lexico_semantico.ipynb  # Preprocesamiento, embeddings, LDA y coherencia
│   └── analisis_sintactico.ipynb        # POS tagging, patrones verbales y complejidad oracional
├── docs/
│   └── registro_cambios.docx          # Registro de revisiones del artículo
└── README.md
```

## Corpus

El estudio trabaja con tres corpus de textos académicos en español sobre creatividad y educación (artículos publicados entre 2010 y 2018):

| Corpus  | Fuente                                        | Palabras |
|---------|-----------------------------------------------|----------|
| Humano  | Artículos recolectados vía SerpAPI            | 44.527   |
| ChatGPT | Generado con GPT-5 (sept–oct 2025)            | 29.398   |
| Copilot | Generado con Copilot / GPT-4o (sept–oct 2025) | 13.159   |

Cada corpus incluye resumen, introducción y conclusiones de 52 artículos (156 textos por corpus, 468 en total).

> **Nota:** Los corpus no se distribuyen en este repositorio por derechos de autor sobre los artículos originales.

## Formato de entrada

Ambos notebooks esperan un archivo Excel con la siguiente estructura:

| Columna       | Descripción                        |
|---------------|------------------------------------|
| `Resumen`     | Texto del resumen del artículo     |
| `Introduccion`| Texto de la introducción           |
| `Conclusiones`| Texto de las conclusiones          |

- **Formato**: `.xlsx`
- **Nombre del archivo**: `Corpus_humano.xlsx` (ajustable en la primera celda del notebook)
- **Una fila por artículo**

## Replicación

Los scripts están desarrollados en Google Colaboratory y se ejecutan directamente desde la nube sin instalación local.

1. Abre el notebook correspondiente en [Google Colab](https://colab.research.google.com/)
2. Sube tu archivo `Corpus_humano.xlsx` a la carpeta `/content/` cuando el notebook lo indique
3. Ejecuta las celdas en orden

El prompt completo de generación de los corpus de IA generativa se encuentra en `prompt/prompt_generacion.md`.

## Metodología resumida

- **Léxico**: frecuencia léxica, IVL (V/N × 100), RTTR, Maas, embeddings (`paraphrase-multilingual-MiniLM-L12-v2`) y modelado de tópicos (LDA, 5 tópicos por corpus)
- **Sintáctico**: distribución POS, patrones verbales (tiempo/modo/aspecto via spaCy `es_core_news_sm`), complejidad oracional por número de verbos finitos
- **Coherencia macroestructural**: similitud coseno TF-IDF entre secciones del corpus

## Licencia

Este trabajo se distribuye bajo licencia [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).  
Puedes usar, compartir y adaptar el material siempre que cites la fuente.

## Cita

```
Kristhi, D. (2026). Comparación de patrones léxicos, sintácticos y de coherencia 
macroestructural en textos académicos en español: escritura humana vs. generada por LLM. 
[Tesis de maestría]. Repositorio: https://github.com/kristhinap/ICC_human-vs-llm-spanish-academic
```
