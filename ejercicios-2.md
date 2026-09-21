# Día 2 — GitHub Copilot en VS Code e IntelliJ

## Objetivo del día

Utilizar GitHub Copilot como asistente de programación: completar código, explicar, refactorizar, generar pruebas y trabajar mediante chat. Los ejercicios extra presentan Cline con un modelo local, Lovable y ComfyUI.

> Regla general: el código generado por una IA no se considera correcto hasta que lo entiendes, lo ejecutas y lo revisas.

> Puedes usar el lenguaje de programación que prefieras para los ejercicios.

---

## Ejercicio 1. VS Code: tu primera sugerencia de código

### Objetivo

Aprender a provocar y revisar una sugerencia en línea de GitHub Copilot.

### Tarea

Crea un archivo `calculadora.py` y escribe:

```python
def calcular_media(numeros):
    # Devuelve la media de una lista de números.
```

Espera una sugerencia de Copilot.

Después escribe tú mismo o con Copilot:

```python
datos = [5, 7, 9, 10]
print(calcular_media(datos))
```

### Comprobaciones

- ¿Qué ocurre si la lista está vacía?
- ¿La función es fácil de entender?
- ¿Aceptarías la primera sugerencia sin modificar nada?

---

## Ejercicio 2. VS Code: explicar código existente

### Objetivo

Usar Copilot Chat para entender código antes de modificarlo.

### Código

```python
def procesar(precios):
    total = 0
    for p in precios:
        if p > 0:
            total += p * 1.21
    return round(total, 2)
```

### Tarea

Pide a Copilot:

1. Que explique qué hace el código paso a paso.
2. Que indique qué representa probablemente `1.21`.
3. Que proponga nombres más claros.
4. Que señale casos que deberían validarse.

---

## Ejercicio 3. VS Code: refactorización guiada

### Objetivo

Aprender a pedir mejoras concretas sin cambiar el comportamiento esperado.

### Código inicial

```python
def f(a):
    r = []
    for x in a:
        if x % 2 == 0:
            r.append(x * 2)
    return r
```

### Tarea

Pide a Copilot que:

- use nombres descriptivos;
- añada un docstring;
- mantenga el mismo resultado;
- explique cada cambio;
- no introduzca librerías externas.

### Pregunta final

¿El código "más corto" es necesariamente mejor?

---

## Ejercicio 4. VS Code: generar pruebas

### Objetivo

Usar Copilot para proponer casos de prueba y detectar casos límite.

### Código

```python
def es_mayor_de_edad(edad):
    return edad >= 18
```

### Tarea

Pide a Copilot que genere pruebas para:

- 17;
- 18;
- 19;
- un número negativo;
- un texto;
- `None`.

Después pregunta a Copilot si la función debería validar entradas.

> No aceptes una prueba como válida solo porque la haya generado Copilot.

---

## Ejercicio 5. VS Code: mini funcionalidad con Copilot Chat

### Objetivo

Pasar de una descripción en lenguaje natural a una pequeña implementación.

### Tarea

Crea un programa de consola que gestione una lista de tareas.

Debe permitir:

1. añadir una tarea;
2. listar tareas;
3. marcar una tarea como completada;
4. salir.

### Condiciones

Pide a Copilot que:

- use Python (o el lenguaje que prefieras);
- no use librerías externas;
- mantenga el código sencillo;
- divida el programa en funciones;
- explique cómo ejecutarlo.

---

## Ejercicio 6. IntelliJ: primera sugerencia en Java

### Objetivo

Usar las sugerencias de GitHub Copilot dentro de IntelliJ.

### Tarea

Crea una clase:

```java
public class ConversorTemperatura {

    // Convierte grados Celsius a Fahrenheit
}
```

Deja que Copilot proponga el método.

Añade después un segundo comentario:

```java
// Convierte Fahrenheit a Celsius
```

### Revisión

Comprueba manualmente al menos estos valores:

- 0 ºC → 32 ºF
- 100 ºC → 212 ºF

---

## Ejercicio 7. IntelliJ: comprender y mejorar una clase

### Objetivo

Combinar explicación, revisión y refactorización.

### Código inicial

```java
public class Pedido {
    public double calcular(double precio, int cantidad, boolean vip) {
        double total = precio * cantidad;
        if (vip) {
            total = total * 0.9;
        }
        return total;
    }
}
```

### Tarea

Pide a Copilot que:

1. explique la clase;
2. indique posibles problemas de validación;
3. proponga nombres más explícitos;
4. añada JavaDoc;
5. genere 4 casos de prueba.

---

## Ejercicio 8. EXTRA — LM Studio + Cline en VS Code

### Objetivo

Probar un asistente de programación conectado a un modelo local.

### Requisitos

- VS Code.
- Cline instalado.
- LM Studio funcionando con un modelo compatible con tu equipo.

### Tarea

Crea una carpeta vacía y pide a Cline:

```text
Crea una página web muy sencilla con HTML, CSS y JavaScript.
Debe mostrar un contador con botones +1, -1 y Reiniciar.
Antes de modificar archivos, explícame brevemente qué archivos vas a crear.
Mantén el código simple porque estoy aprendiendo.
```

### Revisión obligatoria

Antes de aceptar cambios:

- revisa los archivos que propone;
- lee el JavaScript;
- ejecuta la página;
- comprueba los tres botones.

---

## Ejercicio 9. EXTRA — Lovable: prototipo sin empezar por código

### Objetivo

Comprobar cómo una descripción funcional puede convertirse en una aplicación.

### Tarea

Pide a Lovable una pequeña web para registrar libros pendientes de leer.

Debe incluir:

- título de la aplicación;
- campo para nombre del libro;
- campo para autor;
- botón "Añadir";
- lista de libros;
- opción para marcar un libro como leído;
- diseño sencillo y legible.

### Segunda iteración

Pide tres cambios por separado:

1. añade un filtro "Todos / Pendientes / Leídos";
2. mejora el aspecto visual;
3. muestra un contador de libros pendientes.

¿Qué diferencia encuentras entre pedir una aplicación a Lovable y pedir código a GitHub Copilot?

---

## Ejercicio 10. EXTRA — ComfyUI: entender un flujo por nodos

### Objetivo

Comprender la lógica básica de una interfaz de IA generativa basada en nodos.

### Tarea

Abre un workflow básico de generación de imagen disponible en tu instalación.

Identifica visualmente qué parte del flujo corresponde a:

- modelo;
- prompt positivo;
- prompt negativo, si existe;
- generación o muestreo;
- salida o guardado de imagen.

Genera una imagen con un prompt sencillo, por ejemplo:

```text
A small retro robot reading a book in a quiet library, warm light, simple illustration
```

### Segunda iteración

Cambia únicamente una variable, por ejemplo:

- el prompt;
- la semilla;
- el tamaño;
- algún otro parámetro de generación.

> No es necesario comprender todos los nodos. El objetivo es entender que el resultado se obtiene mediante un flujo de operaciones conectadas.
