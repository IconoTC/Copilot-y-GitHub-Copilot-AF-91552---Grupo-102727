# Día 4 — Microsoft 365 Copilot, agentes, GitHub Actions y Docker

## Objetivo del día

Aplicar IA a herramientas habituales de Microsoft 365, crear un agente sencillo y terminar con una introducción práctica a GitHub Actions y Docker ayudándose de GitHub Copilot.

> Las funciones disponibles pueden variar según la licencia y la configuración de cada organización. Si una función concreta no está habilitada, realiza el ejercicio con datos ficticios o en otra herramienta similar.

---

## Ejercicio 1. Word + Copilot: convertir notas en un documento

### Objetivo

Usar Copilot para estructurar y mejorar un documento.

### Notas de partida

```text
Proyecto: actualización de la intranet.
Objetivo: que sea más fácil encontrar documentación.
Problemas actuales: demasiadas carpetas, nombres poco claros, documentos duplicados.
Primera propuesta: reorganizar por departamentos, definir responsables y archivar versiones antiguas.
Plazo aproximado: 6 semanas.
```

### Tarea

En Word, pide a Copilot que convierta las notas en un documento breve con:

- título;
- objetivo;
- situación actual;
- propuesta;
- próximos pasos;
- riesgos.

Después pide una segunda versión más ejecutiva y de máximo una página.

---

## Ejercicio 2. PowerPoint + Copilot: presentar una idea

### Objetivo

Transformar contenido escrito en una presentación comprensible.

### Tarea

Usa el contenido del ejercicio anterior para crear una presentación de **5–6 diapositivas**.

Debe incluir:

1. Portada.
2. Problema actual.
3. Objetivo.
4. Propuesta.
5. Plan aproximado.
6. Próximos pasos.

Comprueba:

- ¿hay demasiado texto?
- ¿los títulos cuentan una historia?
- ¿alguna diapositiva se puede simplificar?
- ¿hay información que Copilot haya añadido sin estar en las notas?

---

## Ejercicio 3. Excel + Copilot: preguntar sobre datos

### Objetivo

Utilizar lenguaje natural para analizar una tabla sencilla.

### Datos de ejemplo

Introduce esta tabla en Excel y conviértela en una tabla de Excel:

| Mes     | Ventas | Gastos | Incidencias |
| ------- | -----: | -----: | ----------: |
| Enero   |  12000 |   8000 |          12 |
| Febrero |  13500 |   8200 |           9 |
| Marzo   |  11800 |   7900 |          16 |
| Abril   |  15100 |   9100 |           7 |
| Mayo    |  14900 |   8700 |           6 |

### Tarea

Pide a Copilot:

1. calcular el beneficio mensual;
2. identificar el mes con mayor beneficio;
3. indicar el mes con más incidencias;
4. proponer un gráfico útil;
5. explicar qué conclusión **sí** puede obtenerse con esos datos y cuál **no**.

---

## Ejercicio 4. Edge + Copilot: resumir una página sin dejar de leer la fuente

### Objetivo

Usar Copilot como apoyo a la lectura, no como sustituto de la comprobación.

### Tarea

Abre en Edge una página informativa no sensible elegida por el profesor.

Pide:

1. un resumen en 5 puntos;
2. tres conceptos clave;
3. una explicación para una persona principiante;
4. tres preguntas que todavía quedarían abiertas.

### Comprobación

Busca manualmente en la página dos afirmaciones del resumen.

---

## Ejercicio 5. Outlook + Copilot: resumir y responder

### Objetivo

Practicar resumen de conversación y redacción de respuesta.

### Hilo ficticio

```text
De: Laura
Necesitamos cerrar la fecha de la formación. El cliente propone martes o jueves de la semana que viene.

De: Marcos
El martes no puedo por la mañana, pero sí a partir de las 16:00. El jueves estoy disponible.

De: Laura
Perfecto. También necesitamos confirmar si la sesión será presencial o por Teams.

De: Cliente
Preferimos el jueves a las 10:00 y, si es posible, presencial.
```

### Tarea

Pide a Copilot:

1. resumir el hilo;
2. extraer decisiones y pendientes;
3. redactar una respuesta profesional confirmando lo que ya está claro y preguntando únicamente por lo que falte.

### Revisión

¿Copilot inventó algún acuerdo que no estuviera en el hilo?

---

## Ejercicio 6. Copilot Studio: agente FAQ básico

### Objetivo

Crear un primer agente con instrucciones y conocimiento limitado.

> Si no tienes acceso a Copilot Studio, puedes usar Relevance AI.

### Escenario

Crea un agente llamado **Asistente de Formación Demo**.

Información ficticia:

```text
Horario de atención: lunes a viernes, de 9:00 a 14:00.
Modalidad de los cursos: presencial y online.
Certificados: se entregan al finalizar el curso si se cumplen los requisitos de asistencia.
Contacto: formacion@empresa-demo.local
```

### Instrucciones recomendadas

El agente debe:

- responder solo sobre la información proporcionada;
- reconocer cuando no conoce una respuesta;
- no inventar precios, fechas ni condiciones;
- responder con lenguaje sencillo.

### Pruebas

Pregunta:

1. ¿Cuál es el horario?
2. ¿Hay cursos online?
3. ¿Cuánto cuesta el curso de Python?
4. ¿Puedo obtener certificado?
5. ¿Cuál es el teléfono?

### Revisión

Las preguntas 3 y 5 no están respondidas por el conocimiento proporcionado. Comprueba cómo reacciona el agente.

---

## Ejercicio 7. Copilot Studio: mejorar las instrucciones del agente

### Objetivo

Aprender que un agente necesita reglas claras, no solo una fuente de información.

### Tarea

Amplía las instrucciones del agente anterior:

- Si conoce la respuesta, debe contestar en máximo 5 líneas.
- Si falta información, debe decir claramente que no está disponible.
- No debe inventar datos.
- Si la pregunta no está relacionada con formación, debe indicarlo.
- Debe terminar las respuestas válidas con una sugerencia de siguiente paso cuando sea útil.

### Pruebas

Haz al menos 6 preguntas:

- 2 claramente respondibles;
- 2 no respondibles;
- 2 fuera de tema.

---

## Ejercicio 8. Relevance AI — alternativa para quien no tenga Copilot Studio

### Objetivo

Crear un agente sencillo en una plataforma alternativa de agentes.

### Tarea

Reproduce el **Asistente de Formación Demo** del ejercicio 6 en Relevance AI.

Configura:

- nombre;
- objetivo;
- instrucciones;
- información de referencia;
- comportamiento cuando no conoce la respuesta.

### Pruebas

Usa las mismas cinco preguntas del ejercicio 6.

> Si no tienes acceso a Copilot Studio, compara Relevance AI con el comportamiento esperado definido en el ejercicio 6.

---

## Ejercicio 9. GitHub Copilot + GitHub Actions: primer workflow

### Objetivo

Entender que GitHub Actions ejecuta automáticamente tareas definidas en archivos YAML.

### Situación

Tienes un repositorio con un pequeño proyecto Python.

### Tarea

Pide a GitHub Copilot que te ayude a crear:

```text
.github/workflows/python-check.yml
```

Requisitos:

- ejecutarse al hacer `push`;
- usar un runner Linux;
- descargar el código del repositorio;
- configurar Python;
- ejecutar `python --version`;
- si existe un archivo de pruebas, dejar preparado un paso claramente identificado para ejecutarlas.

### Muy importante

Antes de guardar el YAML, pide a Copilot que explique:

- qué significa `on`;
- qué es un `job`;
- qué es un `step`;
- qué hace `uses`;
- qué hace `run`.

### Ampliación

Si dispones de un repositorio de prueba, haz un `push` y observa la pestaña **Actions**.

---

## Ejercicio 10. GitHub Copilot + Docker: primer Dockerfile

### Objetivo

Comprender los elementos básicos de un `Dockerfile`.

### Proyecto de ejemplo

Crea:

`app.py`

```python
print("Hola desde mi primer contenedor")
```

### Tarea

Pide a GitHub Copilot que genere un `Dockerfile` mínimo para ejecutar ese archivo.

Antes de aceptarlo, debe explicarte:

- `FROM`;
- `WORKDIR`;
- `COPY`;
- `CMD`.

### Revisión

Comprueba que:

- utiliza una imagen base apropiada;
- no instala dependencias innecesarias;
- copia únicamente lo necesario para este ejemplo;
- el comando final ejecuta `app.py`.

### Si tienes Docker instalado

Construye y ejecuta la imagen.

### Si no tienes Docker instalado

Realiza el ejercicio de revisión del `Dockerfile` sin ejecutar los comandos.

---
