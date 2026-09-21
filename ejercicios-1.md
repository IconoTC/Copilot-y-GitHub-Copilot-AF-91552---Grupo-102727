# Día 1 — Copilot Chat, ecosistema Copilot y prompting

## Objetivo del día

Familiarizarse con las principales herramientas llamadas "Copilot", aprender a usar Copilot Chat de forma segura y comenzar a escribir prompts claros mediante frameworks.

> Regla general: no uses datos reales de clientes, contraseñas, información personal ni documentación confidencial. Revisa siempre las respuestas generadas por la IA antes de darlas por correctas.

---

## Ejercicio 1. ¿Qué Copilot usarías?

### Objetivo

Distinguir entre Copilot Chat, Microsoft 365 Copilot, GitHub Copilot y Copilot Studio.

### Tarea

Indica qué herramienta usarías principalmente en cada situación:

1. Quieres que una IA te ayude a escribir una función en Python dentro de VS Code.
2. Quieres resumir un documento de Word de tu organización.
3. Quieres hacer una consulta general a una IA desde el navegador.
4. Quieres crear un agente que responda preguntas frecuentes de una empresa.
5. Quieres recibir sugerencias de código mientras escribes Java en IntelliJ.
6. Quieres preparar un borrador de correo utilizando información de tu entorno Microsoft 365.

---

## Ejercicio 2. Primer contacto con Copilot Chat

### Objetivo

Aprender a mantener una conversación sencilla con Copilot Chat.

### Tarea

Realiza estas tres peticiones:

1. `Explícame qué es la inteligencia artificial generativa.`
2. Pide que vuelva a explicarlo para una persona que nunca ha trabajado con IA.
3. Pide que lo resuma finalmente en 5 ideas.

---

## Ejercicio 3. De un prompt vago a un prompt útil

### Objetivo

Comprobar cómo influyen el contexto, el objetivo y el formato.

### Tarea

Prueba primero este prompt:

```text
Hazme un resumen sobre ciberseguridad.
```

Después crea una versión mejorada que incluya:

- público objetivo;
- finalidad;
- extensión;
- formato de salida;
- temas que debe incluir;
- nivel técnico.

---

## Ejercicio 4. Framework RACE

### Objetivo

Practicar **RACE = Role – Action – Context – Explanation**.

### Situación

Tienes que explicar qué es el phishing a una persona administrativa sin conocimientos técnicos.

### Tarea

Construye un prompt con esta estructura:

```text
Role:
Action:
Context:
Explanation:
```

Pide que incluya:

- explicación sencilla;
- un ejemplo ficticio;
- tres señales de alerta;
- tres recomendaciones de prevención.

### Revisión

Comprueba si la respuesta realmente está adaptada al nivel del público.

---

## Ejercicio 5. TAG frente a APE

### Objetivo

Ver cómo dos frameworks pueden resolver tareas parecidas con distinta cantidad de contexto.

### Parte A — TAG

Usa **TAG = Task – Action – Goal** para pedir a Copilot que convierta estas notas en una lista de tareas:

```text
Reunión proyecto Alfa:
- Falta revisar presupuesto.
- Marta enviará la documentación.
- Hay que preparar la demo del viernes.
- El cliente ha pedido cambiar el texto de la página inicial.
```

### Parte B — APE

Repite la tarea usando **APE = Action – Purpose – Execution**, pidiendo ahora una tabla con:

- tarea;
- responsable;
- prioridad;
- fecha o plazo si aparece en las notas.

---

## Ejercicio 6. Elige el framework adecuado

### Objetivo

Aprender a seleccionar un framework según la tarea.

### Frameworks disponibles

- RACE
- CARE
- APE
- CREATE
- TAG
- CREO
- RISE
- PAIN
- COAST
- ROSES

### Tarea

Elige un framework para cada situación y justifica tu decisión en una frase:

1. Explicar Git a una persona que empieza.
2. Redactar un correo siguiendo un ejemplo de tono.
3. Analizar por qué se están retrasando varias tareas.
4. Preparar un plan de trabajo de tres días.
5. Crear una solución completa para organizar el onboarding de nuevos empleados.
6. Pedir una acción muy corta y directa.

---

## Ejercicio 7. CREATE: un prompt completo

### Objetivo

Construir un prompt detallado sin necesidad de escribir instrucciones desordenadas.

### Situación

Quieres preparar una pequeña guía titulada **"Cómo empezar a usar IA en el trabajo sin cometer errores básicos"**.

### Tarea

Usa:

**CREATE = Character – Request – Examples – Adjustment – Type – Extras**

El resultado debe:

- estar dirigido a personas principiantes;
- utilizar lenguaje sencillo;
- incluir 5 buenas prácticas;
- incluir 3 errores frecuentes;
- terminar con una checklist;
- entregarse en Markdown.

---

## Ejercicio 8. Revisar críticamente una respuesta de IA

### Objetivo

Evitar aceptar automáticamente todo lo que responde Copilot.

### Tarea

Pide a Copilot:

```text
Dame 8 recomendaciones para implantar IA generativa en una pequeña empresa.
```

Después revisa la respuesta con esta checklist:

- [ ] ¿Ha hecho alguna afirmación que debería comprobar?
- [ ] ¿Ha supuesto información que yo no le había dado?
- [ ] ¿Hay recomendaciones demasiado genéricas?
- [ ] ¿Incluye posibles riesgos?
- [ ] ¿Distingue entre información sensible y no sensible?
- [ ] ¿El formato es útil?
- [ ] ¿Hay algo que no entiendo y debería pedir que explique?

Finalmente, escribe un segundo prompt para mejorar la primera respuesta.

---

## Ejercicio 9. EXTRA — LM Studio: IA local

### Objetivo

Experimentar con un modelo ejecutado localmente y compararlo con una herramienta en la nube.

### Requisito

LM Studio instalado y un modelo pequeño que el equipo pueda ejecutar.

### Tarea

Ejecuta en LM Studio este prompt:

```text
Explica qué es una contraseña segura a una persona que no tiene conocimientos técnicos.
Devuelve:
1. Una explicación de máximo 100 palabras.
2. Cinco recomendaciones.
3. Dos errores frecuentes.
```

Ejecuta exactamente el mismo prompt en Copilot Chat.

Haz una comparación breve:

| Aspecto          | LM Studio | Copilot Chat |
| ---------------- | --------- | ------------ |
| Claridad         |           |              |
| Velocidad        |           |              |
| Nivel de detalle |           |              |
| Facilidad de uso |           |              |

### Pregunta final

¿Qué ventajas e inconvenientes percibes al ejecutar un modelo local?

---

## Ejercicio 10. EXTRA — Gamma: presentación desde un prompt

### Objetivo

Generar y revisar una presentación con IA.

### Tarea

En Gamma, crea una presentación de **6 diapositivas** sobre:

**"Buenas prácticas para usar IA generativa en el trabajo"**

Incluye como mínimo:

1. Portada.
2. Qué puede hacer la IA.
3. Cómo escribir mejores prompts.
4. Privacidad y datos sensibles.
5. Necesidad de revisar las respuestas.
6. Checklist final.

### Segunda iteración

Usa las funciones de edición con IA para:

- reducir texto;
- mejorar un título;
- cambiar la estructura de una diapositiva;
- revisar si el diseño ayuda a entender el contenido.
