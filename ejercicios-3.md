# Día 3 — Sesgos en la IA, NotebookLM y Make

## Objetivo del día

Comprender de forma práctica cómo pueden aparecer sesgos en los datos y en las respuestas de IA, aprender a revisar críticamente resultados y utilizar NotebookLM para trabajar con fuentes. Make se introduce como ejercicio extra de automatización.

> Importante: observar una respuesta sesgada en un ejercicio no permite concluir cómo funciona todo un modelo. El objetivo es aprender a detectar riesgos, formular hipótesis y comprobar resultados con más evidencia.

---

## Ejercicio 1. ¿Está equilibrado el dataset?

### Objetivo

Identificar un posible sesgo de representación.

### Dataset ficticio

Una empresa quiere entrenar un sistema para recomendar cursos internos.

| Departamento   | Personas en el dataset |
| -------------- | ---------------------: |
| Desarrollo     |                    600 |
| Administración |                     80 |
| Soporte        |                     70 |
| Ventas         |                     50 |

### Tarea

Responde:

1. ¿Qué grupo está sobrerrepresentado?
2. ¿Qué grupos están infrarrepresentados?
3. ¿Qué podría ocurrir si el sistema aprende principalmente de este dataset?
4. ¿Qué información adicional pedirías antes de utilizarlo?
5. Propón dos formas de mejorar el dataset.

---

## Ejercicio 2. El problema de las categorías que damos por "normales"

### Objetivo

Entender que el propio lenguaje y la forma de etiquetar datos pueden introducir sesgos.

### Situación

Un dataset de productos contiene estas etiquetas:

```text
sandía
sandía amarilla
tomate
tomate amarillo
arroz
arroz integral
```

### Tarea

Analiza:

- ¿Por qué algunas variantes reciben un adjetivo y otras se consideran la categoría "normal"?
- ¿Qué puede aprender un modelo de estas decisiones?
- Propón una forma más explícita de etiquetar el color o variedad sin asumir una opción por defecto.

---

## Ejercicio 3. Variante lingüística y corrección automatizada

### Objetivo

Reflexionar sobre sesgos provocados por diferencias lingüísticas.

### Situación

Un sistema de corrección automática ha sido entrenado sobre todo con una única variedad del español.

### Tarea

Imagina cinco expresiones perfectamente válidas en distintas regiones hispanohablantes que un sistema podría considerar "raras" o intentar sustituir.

Después responde:

1. ¿Es un error gramatical o una diferencia de variante?
2. ¿Qué problema habría si el sistema presentara siempre una variante como la única correcta?
3. ¿Cómo debería diseñarse una herramienta más respetuosa con distintas variantes del idioma?

---

## Ejercicio 4. Riesgo según el dominio

### Objetivo

Comprender que un error de IA no tiene las mismas consecuencias en todos los contextos.

### Tarea

Ordena estas aplicaciones **por impacto potencial de un error**, pero no busques una respuesta única: justifica el criterio utilizado.

- Recomendar una película.
- Corregir un texto informal.
- Evaluar una solicitud de crédito.
- Ayudar a interpretar una prueba médica.
- Controlar parte de un vehículo autónomo.
- Recomendar el orden de canciones de una playlist.

### Puesta en común

Comparad criterios entre grupos.

---

## Ejercicio 5. IA confiable: cuatro preguntas

### Objetivo

Aplicar los conceptos de seguridad, privacidad, explicabilidad y equidad.

### Situación

Una empresa quiere usar una IA para priorizar automáticamente solicitudes de atención al cliente.

### Tarea

Formula al menos dos preguntas para cada dimensión:

#### Seguridad de datos

- ¿...?
- ¿...?

#### Privacidad de datos

- ¿...?
- ¿...?

#### Explicabilidad

- ¿...?
- ¿...?

#### Equidad

- ¿...?
- ¿...?

---

## Ejercicio 6. Auditoría básica de una respuesta generativa

### Objetivo

Buscar patrones o estereotipos sin convertir una única prueba en una conclusión definitiva.

### Tarea

Usa una herramienta de IA y pide:

```text
Inventa un equipo ficticio de 10 personas para una empresa tecnológica.
Indica para cada persona un nombre, un puesto y una frase sobre sus responsabilidades.
No uses personas reales.
```

Analiza el resultado:

- variedad de puestos;
- distribución de responsabilidades;
- posibles estereotipos;
- nombres o perfiles repetitivos;
- roles de liderazgo;
- información que el modelo haya supuesto sin que se la pidieras.

### Segunda iteración

Escribe un prompt más controlado para conseguir un equipo deliberadamente diverso en perfiles profesionales y responsabilidades, sin pedir atributos personales sensibles.

---

## Ejercicio 7. NotebookLM: crear un cuaderno basado en fuentes

### Objetivo

Aprender a trabajar con una IA centrada en documentos suministrados por el usuario.

### Tarea

Crea un cuaderno en NotebookLM y añade como fuentes los materiales del curso que el profesor indique, por ejemplo:

- material de frameworks de prompting;
- material sobre sesgos en la IA.

Pregunta:

1. ¿Qué es un framework de prompting?
2. ¿Qué ventajas aporta estructurar un prompt?
3. ¿Qué es un sesgo en un dataset?
4. ¿Qué consecuencias puede tener un dataset desbalanceado?

### Revisión

Comprueba manualmente que al menos dos afirmaciones estén realmente respaldadas por el documento citado.

---

## Ejercicio 8. NotebookLM: estudiar sin inventar contenido

### Objetivo

Aprovechar una misma fuente para generar distintos materiales de estudio.

### Tarea

Usa el mismo cuaderno del ejercicio anterior y pide tres productos diferentes:

1. Un resumen de máximo 10 puntos.
2. 8 preguntas de repaso con respuesta.
3. Un glosario de 10 conceptos.

Si tu versión de NotebookLM ofrece mapas conceptuales, resúmenes de audio o vídeo, prueba uno de ellos como ampliación.

### Pregunta final

¿En qué producto detectaste que NotebookLM condensaba mejor la información de las fuentes?

---

## Ejercicio 9. NotebookLM: pregunta fácil, pregunta difícil, pregunta no respondible

### Objetivo

Aprender a distinguir entre información presente en las fuentes y cuestiones que requieren información externa.

### Tarea

Formula:

1. Una pregunta cuya respuesta aparezca claramente en los documentos.
2. Una pregunta que obligue a combinar información de varias partes.
3. Una pregunta que los documentos **no puedan responder**.

Para cada pregunta, observa:

- respuesta obtenida;
- fuente utilizada;
- si la respuesta estaba realmente respaldada;
- cómo reaccionó NotebookLM cuando faltaba información.

---

## Ejercicio 10. EXTRA — Make: filtrar correos y enviar una notificación

### Objetivo

Comprender un flujo sencillo de automatización utilizando tres elementos básicos de Make:

**recibir → filtrar → actuar**

### Situación

Queremos crear una automatización que revise los correos recibidos.

Si el asunto del correo contiene la palabra:

```text
URGENTE
```

Make debe enviar automáticamente un nuevo correo de aviso.

### Flujo

```text
Llega un correo
↓
Comprobar el asunto
↓
¿Contiene "URGENTE"?
↓
Sí → Enviar correo de aviso
No → No hacer nada
```

### Tarea

Crea un escenario en Make con los siguientes pasos:

1. Añade un módulo para detectar nuevos correos recibidos.
2. Añade un filtro que compruebe si el asunto contiene la palabra `URGENTE`.
3. Si se cumple la condición, añade un módulo para enviar un nuevo correo.
4. Configura el correo automático con un mensaje parecido a este:

```text
Asunto: Aviso de correo urgente

Se ha recibido un nuevo correo marcado como urgente.

Asunto original: [asunto del correo recibido]

Remitente: [remitente]
```

### Prueba 1 — El filtro debe cumplirse

Envíate un correo con este asunto:

```text
URGENTE - Problema con el servidor
```

Ejecuta el escenario y comprueba que Make detecta el correo y envía automáticamente el correo de aviso.

### Prueba 2 — El filtro no debe cumplirse

Envíate otro correo con este asunto:

```text
Reunión del viernes
```

Ejecuta de nuevo el escenario.

Comprueba que Make detecta el correo, pero el filtro impide que se envíe el correo de aviso.

### Entregable

Realiza una captura del escenario creado en Make.

Después completa:

```text
Disparador:
Cuando llega un nuevo correo.

Filtro:
El asunto contiene "URGENTE".

Acción:
Enviar un correo de aviso.

Correo de prueba que activa el flujo:
____________________________________

Correo de prueba que NO activa el flujo:
____________________________________
```

### Preguntas finales

1. ¿Para qué sirve el filtro?
2. ¿Qué ocurriría si eliminásemos el filtro?
3. ¿Cómo modificarías el escenario para detectar también la palabra `IMPORTANTE`?
4. ¿Qué otros datos de un correo podríamos utilizar para crear filtros?

Por ejemplo:

- Remitente.
- Palabras del asunto.
- Destinatario.
- Existencia de archivos adjuntos.
- Contenido del mensaje.

### Ampliación opcional

Modifica el flujo para que el correo de aviso solo se envíe cuando se cumplan dos condiciones:

```text
El asunto contiene "URGENTE"

Y

el remitente es una dirección de correo concreta
```

Por ejemplo:

```text
Asunto contiene: URGENTE

Y

Remitente es: profesor@ejemplo.com
```

### Resultado esperado

Al terminar el ejercicio deberías tener un flujo parecido a este:

```text
Nuevo correo recibido
        ↓
Filtro: asunto contiene "URGENTE"
        ↓
      ¿Sí?
        ↓
Enviar correo de aviso
```

El objetivo del ejercicio es entender que una automatización sencilla en Make puede construirse utilizando:

**un disparador + una condición + una acción**.
