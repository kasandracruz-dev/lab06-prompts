# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts. 
Herramienta de IA usada: Gemini 
- [Bitacora de prompts](prompts/BITACORA.md)
- [Tarea: Diseño e Iteración de Prompt Profesional](prompts/Tarea.md)
## Ejercicio 2: Tokens y ventana de contexto
| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. |36 |8 |
| The students program in Java. |31 |7 |
| desafortunadamente |18 | 4|


## Ejercicio 3: Temperatura
| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0           |100.0%          |BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5         |65.3%           |BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 1           |44.5%           |BiblioTec, PrestaLibro, LibroYa, LibroYa, PrestaLibro |
| 1.8         |32.2%           |BiblioTec, PrestaLibro, LibroYa, LibroYa, PrestaLibro |

Al aumentar la temperatura, las probabilidades de todas las opciones se equilibran y aumentan los nombres seleccionados en cada intento.

El simulador nunca inventa un nombre nuevo porque sus salidas se limitan estrictamente a los elementos predefinidos en el arreglo opciones.

## Ejercicio 4: Prompt vago vs estructurado 
| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema |No | Si|
| Menciona a los usuarios principales |No |Si |
| Tiene exactamente 3 funcionalidades |No |Si|
| Esta en 3 parrafos |No |Si |
| Lo usaria en un informe real |No |Si|


## Ejercicio 5: Anatomia de un prompt
| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol        |Actua como desarrollador Java|
| Instruccion|Crea un programa en Java para gestionar los productos de una tienda usando una clase |
| Contexto   |Producto con los atributos codigo, nombre, precio y stock |
| Ejemplo    |Explica primerola estructura de la clase y luego presenta el codigo Java |
| Formato    |Usa este estilopara los metodos:getPrecio(), setPrecio(double precio) |

- Nivel 1:Genera un programa en Java genérico y básico por falta de detalles.
- Nivel 2:Incluye buenas prácticas de desarrollo, comentarios profesionales y una mejor estructura de código.
- Nivel 3:Enfoca el programa específicamente en la gestión de una tienda y sus productos.
- Nivel 4:Define con precisión la clase Producto usando los atributos solicitados
- Nivel 5:Organiza la respuesta en dos partes claras: primero una explicación teórica de la estructura y luego el código fuente.

## Ejercicio 6: Del prompt basico al profesional
| Qué revisar | Cumple (Sí / No) |
|------------ |--------------------|
|¿Está escrito en Java y usa Swing?|Si|
|¿Pide correo y contraseña?|Si|
|¿Explica el funcionamiento antes o después del código?|Si|
|¿El código está organizado en clases?|Si|
|¿Valida los datos que ingresa el usuario?|Si|

```
PROMPT PROFESIONAL
Actua como desarrollador
Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases. 

MEJORA
Mejora el codigo anterior con estas restricciones: no uses librerias externas, valida que el correo contenga @ y que la contrasena tenga al menos 8 caracteres, y muestra los mensajes con JOptionPane.

```
