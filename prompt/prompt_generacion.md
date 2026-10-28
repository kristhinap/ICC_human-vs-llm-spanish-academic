# Prompt de generación de corpus LLM

Este archivo contiene el prompt utilizado para generar los corpus de ChatGPT y Copilot en el estudio. Se ejecutó de forma iterativa sobre cada uno de los 52 títulos del corpus humano.

---

## Prompt

```
Actúa como un investigador académico especializado en creatividad aplicada a la educación,
creatividad musical y autoestima desde diferentes enfoques teóricos.

Redacta el resumen, la introducción y las conclusiones para un artículo académico cuyo
título es: "[TÍTULO]".

Ten en cuenta las siguientes instrucciones:

- Puedes consultar fuentes en la web, pero no debes reutilizar texto existente; el objetivo
  es producir un trabajo original.
- Si encuentras un artículo publicado con ese mismo título, ignóralo completamente.
- El artículo será publicado en una revista académica, por lo que la redacción debe
  ajustarse a ese registro formal.

Requisitos por sección:

RESUMEN
- Entre 150 y 200 palabras.
- Debe incluir el objetivo, la metodología, los principales hallazgos y la conclusión
  general del artículo.

INTRODUCCIÓN
- Extensión mínima de una página.
- Debe integrar en un texto continuo (sin subtítulos): el objetivo del estudio,
  la justificación de su relevancia y el marco teórico o antecedentes relacionados.

CONCLUSIONES
- Extensión mínima de media página.
- Deben ser concretas y responder directamente al objetivo planteado en la introducción.

REFERENCIAS
- Entre 6 y 10 referencias en formato APA, sin hipervínculo.
- Deben estar integradas en el texto y listadas al final.
```

---

## Modo de uso

El marcador `[TÍTULO]` se reemplazó por el título de cada uno de los 52 artículos del corpus humano. El prompt se ejecutó de forma independiente para cada título, tanto en ChatGPT como en Copilot, generando un texto completo por iteración.

## Herramientas y versiones

| Herramienta | Modelo       | Período de recolección |
|-------------|--------------|------------------------|
| ChatGPT     | GPT-5        | Septiembre–octubre 2025 |
| Copilot     | GPT-4o       | Septiembre–octubre 2025 |

## Parámetros de generación

Se utilizaron los parámetros por defecto de cada interfaz web en el período de recolección. No se modificaron temperatura, top-p ni penalizaciones de frecuencia o presencia.
