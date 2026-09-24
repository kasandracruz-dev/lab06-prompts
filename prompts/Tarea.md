# Tarea: Diseño e Iteración de un Prompt Profesional

**Funcionalidad elegida:** Sistema de Cálculo de Notas para Estudiantes.

---

## 1. Iteración del Prompt

## Versión 1: Prompt Básico
```text
Hazme un programa en Java que calcule las notas de un estudiante.
```
* Qué cambié: Se usó una instrucción directa sin contexto ni especificaciones.

* Por qué: Es el punto de partida inicial para evaluar cómo responde el modelo sin restricciones.

* Qué mejoró / Resultado: El modelo generó un código básico en consola, pero usó variables aleatorias, no validó datos y no estructuró la salida.

## Versión 2:
```text
Crea un programa en Java en un solo archivo que solicite al usuario 3 notas de un estudiante (de 0 a 20), calcule el promedio ponderado (30%, 30%, 40%) y muestre si el estudiante está Aprobado o Desaprobado. Incluye validación de entradas.
```
* Qué cambié: Se especificó el lenguaje (Java), la lógica de negocio (promedio ponderado), la escala de notas (0 a 20) y la validación de datos.

* Por qué: La v1 era demasiado general y no garantizaba que el código fuera funcional según los requerimientos del curso.

* Qué mejoró / Resultado: La respuesta incluyó código más claro y funcional, pero el estilo del código no era profesional y no se definió cómo estructurar la salida final ni el uso de librerías.

## Versión 3: Prompt final
```text
Actúas como un Desarrollador Senior de Java y educador técnico.

Tu tarea es escribir una clase Java independiente para calcular el estado académico de un estudiante según sus calificaciones.

Un instituto técnico necesita un script sencillo para consola en Java puro para registrar 3 evaluaciones continuas de un alumno y determinar su promedio final.

Ejemplo 
Entrada: Nota 1 = 15, Nota 2 = 12, Nota 3 = 18
Salida esperada:
=== REPORTE ACADÉMICO ===
Nota 1 (30%): 15.0
Nota 2 (30%): 12.0
Nota 3 (40%): 18.0
Promedio Final: 15.30
Estado: APROBADO

Proporciona únicamente un bloque de código Java funcional con un método main, comentarios breves explicando la lógica y manejo de excepciones con Scanner. No agregues texto explicativo antes ni después del código.
No utilices librerías externas ni marcos de trabajo (frameworks), usa únicamente las clases estándar del JDK (java.util.Scanner).
```
* Qué cambié: Se agregaron los 5 componentes (Rol, Instrucción, Contexto, Ejemplo y Formato) y se añadió la restricción explícita de no usar librerías externas.

* Por qué: Para obtener una respuesta exacta, limpia y ejecutable sin relleno narrativo sobrante.

* Qué mejoró / Resultado: El código generado fue perfecto, listo para copiar y ejecutar, con un formato de consola alineado al ejemplo e implementado únicamente con Java estándar.

## Componentes del prompt final 
|Componente	|Fragmento del Prompt Final|
|-----------|--------------------------|
|Rol	|Actúas como un Desarrollador Senior de Java y educador técnico.|
|Instrucción	|Tu tarea es escribir una clase Java independiente para calcular el estado académico de un estudiante según sus calificaciones.|
|Contexto	|Un instituto técnico necesita un script sencillo para consola en Java puro para registrar 3 evaluaciones continuas de un alumno y determinar su promedio final.|
|Ejemplo	|Entrada: Nota 1 = 15, Nota 2 = 12, Nota 3 = 18
Salida esperada:
=== REPORTE ACADÉMICO ===
Nota 1 (30%): 15.0
Nota 2 (30%): 12.0
Nota 3 (40%): 18.0
Promedio Final: 15.30
Estado: APROBADO|
|Formato	|Proporciona únicamente un bloque de código Java funcional con un método main, comentarios breves explicando la lógica y manejo de excepciones con Scanner. No agregues texto explicativo antes ni después del código.|

## Evaluacion del resultado

|Criterio de Evaluación	|Cumplimiento (Sí / No)	|Observaciones|
|-----------------------|-----------------------|-------------|
|¿El código generado compila y ejecuta sin errores?	|Sí	|Utiliza sintaxis válida de Java y estándar JDK.|
|¿Aplica las ponderaciones correctamente (30%, 30%, 40%)?	|Sí|	El cálculo refleja exactamente la lógica solicitada.|
|¿Respeta el formato de salida indicado en el ejemplo?	|Sí|	Imprime el reporte con el mismo encabezado y estructura.|
|¿Cumple con la restricción de no usar librerías externas?	|Sí	|Solo importa y usa java.util.Scanner.|
## Errores que evite

* Ser demasiado general:

Cómo se evitó: En la v1 solo pedí "un programa que calcule notas". Lo corregí definiendo la cantidad de notas (3), la escala (0 a 20) y los porcentajes de ponderación exactos (30%, 30%, 40%).

* No indicar el formato de respuesta:

Cómo se evitó: Se especificó explícitamente que la respuesta debía ser únicamente un bloque de código ejecutable en Java, adjuntando una plantilla visual de cómo debía imprimirse la salida en la consola.


