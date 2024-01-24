# TypeScript

Descubre el poder de TypeScript en el desarrollo web.
Este superset de JavaScript mejora proyectos,
elevando la calidad del código. En esta introducción,
proporcionaremos una base sólida para aprovechar
al máximo las capacidades de TypeScript.
¡Bienvenida al mundo de TypeScript!

## Contenido

- [Introduccion a TypeScript](#introduccion-a-typescript)
  - [Definicion y proposito de TypeScript](#definicion-y-proposito-de-typescript)
  - [Tipado de datos](#tipado-de-datos)
  - [Diferencias clave con JavaScript](#diferencias-clave-con-javascript)

- [Instalacion de TypeScript](#instalacion-de-typescript)
  - [Como instalar TypeScript globalmente usando npm](#como-instalar-typescript-globalmente-usando-npm)
 
- [Configuración del Proyecto](#configuracion-del-proyecto)
  - [Archivo de configuracion **tsconfig.json**](#archivo-de-configuracion-tsconfigjson)
  - [Configuracion de opciones esenciales](#configuracion-de-opciones-esenciales)

- [Variables y tipos de datos](#variables-y-tipos-de-datos)
  - [Declaración de variables con let y const](#declaración-de-variables-con-let-y-const)
  - [Tipos basicos: **number**, **string**, **boolean**, **array**](#tipos-basicos-number-string-boolean-array)
 
- [Funciones](#funciones)
  - [Tipado de parametros y retorno de funciones](#tipado-de-parametros-y-retorno-de-funciones)
  - [Declaracion y llamada de funciones](#declaracion-y-llamada-de-funciones)

- [Interfaces](#interfaces)
  - [Definicion de interfaces para estructurar objetos](#definicion-de-interfaces-para-estructurar-objetos)
  - [Uso de interfaces en funciones](#uso-de-interfaces-en-funciones)


 ## Introduccion a TypeScript

### Definicion y proposito de TypeScript

TypeScript, desarrollado por Microsoft,
potencia el desarrollo de software al agregar
un sistema de tipado estático opcional a JavaScript.
Este sistema, que puedes ver como JavaScript con
"superpoderes", permite trabajar con tipos de datos
de manera más explícita, detectando errores en etapas
tempranas y mejorando la calidad del código.
Manteniendo compatibilidad total con JavaScript,
TypeScript brinda claridad estructural, previene
errores y se destaca como herramienta esencial
para proyectos web, equilibrando flexibilidad y
confiabilidad en el desarrollo de software.

> [!NOTE]
> En matemáticas, un superset es un conjunto que
> contiene todos los elementos de otro conjunto.
> En el caso de TypeScript, es un superset de
> JavaScript. Esto significa que todo lo que puedes
> hacer en JavaScript, también puedes hacerlo en
> TypeScript.

### Tipado de datos

El tipado de datos se refiere a la práctica de
asignar un tipo específico a una variable,
parámetro o cualquier entidad en un programa
informático. Los tipos de datos indican el
tipo de valor que puede almacenarse en una
variable, como números, cadenas de texto,
booleanos, entre otros. Los lenguajes de
programación pueden ser de tipado estático,
donde los tipos se definen en tiempo de
compilación, o de tipado dinámico, donde los
tipos se asignan en tiempo de ejecución. El
tipado de datos ayuda a prevenir errores al
asegurar que las operaciones en las variables
sean coherentes con los tipos de datos asignados.

### Diferencias clave con JavaScript

Las diferencias clave entre TypeScript y JavaScript
se centran principalmente en el sistema de tipado y
algunas características adicionales que TypeScript introduce.
A continuación, se destacan estas diferencias:

1. Tipado estático opcional: TypeScript ofrece tipado
estático opcional para detectar errores en etapas
tempranas durante el desarrollo.

2. Compatibilidad con JavaScript:TypeScript es un
superconjunto de JavaScript, permitiendo la integración
gradual en proyectos existentes.

3. Uso de Clases e Interfaces: Permite la declaración de
clases e interfaces para una programación más orientada
a objetos.

4. Compilación a JavaScript: Requiere compilación a JavaScript mediante el compilador de TypeScript (tsc) antes de la ejecución.

5. Adición de tipos de datos: Introduce nuevos
tipos de datos, como enumeraciones y tipos condicionales.

6. Desarrollo más Seguro: Proporciona un desarrollo
más seguro con tipado estático y características que mejoran
la calidad del código.

## Instalacion de TypeScript

### Como instalar TypeScript globalmente usando npm

Para este ejemplo, primero, instala TypeScript
globalmente en tu computadora (recuerda que TypeScript
no se ejecuta, se transpila) ejecutando la siguiente
línea de código:

```bash
npm install -g typescript
```

Luego, crea un nuevo archivo llamado **Hello.ts**,
ábrelo en tu editor de código y escribe el
siguiente código TypeScript:

```ts
function greet(person: string, date: Date) {
  console.log(`Hi ${person}, today is ${date.toDateString()}!`);
}

greet("Maddison", new Date());

```

Posteriormente, en la misma ubicación donde guardaste
**Hello.ts**, ejecuta el siguiente comando:

```bash
tsc -w Hello.ts
```

Como resultado se debió haber creado un nuevo archivo llamado **Hello.js** y el código que contiene es muy similar (pero
no igual) al archivo  **Hello.ts** la diferencia es que el archivo **Hello.js** lo puedes usar para ser ejecutado.

## Configuracion del proyecto
<!-- En contruccion 🚧👷‍♀️ -->

### Archivo de configuracion **tsconfig.json**

### Configuracion de opciones esenciales

## Variables y tipos de datos

### Declaración de variables con **let** y **const**

En TypeScript, la declaración de variables se
realiza mediante las palabras clave **let** y
**const**, las cuales comparten similitudes
con JavaScript pero con la adición de tipado
estático opcional.

- Declaración con `let`:

  - Se utiliza para declarar variables que pueden ser reasignadas.

```ts
let nombre: string = "Ejemplo";
```

- Declaración con `const`:

  - Se utiliza para declarar variables con un valor constante que no puede ser reasignado.

```ts
const edad: number = 25;
```

Estas declaraciones permiten especificar el
tipo de dato que contendrá la variable, mejorando
la claridad y previniendo posibles errores
durante el desarrollo.

### Tipos basicos: **number**, **string**, **boolean**, **array**

En TypeScript, se utilizan tipos básicos
para definir variables con distintos tipos
de datos. Aquí tienes ejemplos de cómo se
utilizan los tipos básicos:

- **number**

  - Representa valores numéricos, ya sean enteros o decimales.

```ts
let edad: number = 32;
```

- **string**

  - Representa valores de texto.

```ts
let nombre: string = "Ada Lovelace";
```

- **boolean**

  - Representa valores lógicos, es decir, **true** o **false**.

```ts
let activo: boolean = false;
```

- **array**

  - Representa un arreglo de elementos del mismo tipo.
  Puedes especificar el tipo de elementos dentro del arreglo.

```ts
let numeros: number[] = [1, 2, 3, 4, 5];
let palabras: string[] = ["uno", "dos", "tres"];
```

Estos tipos básicos proporcionan un mecanismo
sólido para definir y trabajar con diferentes
tipos de datos en TypeScript, contribuyendo a
la robustez y claridad del código.

## Funciones

### Tipado de parametros y retorno de funciones

En TypeScript, el tipado de parámetros y el tipo
de retorno de las funciones se realiza para mejorar
la claridad y la seguridad del código. Aquí te presento
un ejemplo de cómo se aplica el tipado en parámetros y
retorno de funciones:

```ts
// Declaración de una función con tipado en parámetros y tipo de retorno
function sumar(a: number, b: number): number {
    return a + b;
}

// Llamada a la función con argumentos del tipo correcto
let resultado: number = sumar(3, 5);

console.log(resultado);  // Salida: 8
```

En este ejemplo:

- La función **sumar** espera dos parámetros, ambos del tipo **number**.
- El tipo de retorno de la función también está definido como **number**.

Cuando se llama a la función **sumar**, se deben
proporcionar argumentos del tipo correcto, y la
variable **resultado** se declara con el tipo de
retorno esperado. El tipado estático opcional
en TypeScript permite detectar errores durante
la fase de desarrollo y proporciona información
útil sobre los tipos de datos que la función
espera y devuelve.

> [!TIP]
> Si tienes dudas sobre **funciones**, **parametros** o **agumentos**
>revisa [esta informacion](https://curriculum.laboratoria.la/es/topics/javascript/functions/classic)

### Declaracion y llamada de funciones

En TypeScript, la declaración y llamada de funciones
sigue un formato similar al de JavaScript, pero con
la adición de tipado estático opcional. Aquí unos
ejemplos de  cómo realizar la declaración y llamada de funciones en TypeScript:

- Declaración de función

  - Puedes especificar el tipo de los parámetros y el tipo de retorno.

```ts
function saludar(nombre: string): string {
    return `Hola, ${nombre}!`;
}
```

- Llamada de función

  - Al llamar la función, proporciona argumentos
  del tipo esperado y maneja el valor de retorno.

```ts
let mensaje: string = saludar("Grace Murray Hopper");
console.log(mensaje);
```

## Interfaces

### Definicion de interfaces para estructurar objetos

En TypeScript, las interfaces son una herramienta clave
para definir la estructura de objetos y asegurar la coherencia
en la forma de los datos. Aquí tienes un ejemplo de cómo se
define una interfaz para estructurar objetos:

```ts
// Definición de una interfaz para estructurar objetos
interface Persona {
    nombre: string;
    edad: number;
    email?: string; // Propiedad opcional
}

// Uso de la interfaz para crear objetos que sigan su estructura
let usuaria: Persona = {
    nombre: "Hedy Lamarr",
    edad: 32,
    email: "hedy@example.com"
};
```

En este ejemplo:

- La interfaz **Persona** define la estructura de un objeto que debe
tener propiedades como **nombre** y **edad**, y opcionalmente puede
tener la propiedad **email**.
- Se utiliza la interfaz **Persona** para definir la forma
del objeto **usuaria**.

El uso de interfaces facilita la creación de código más legible,
mantenible y seguro al definir claramente la estructura de los
objetos en TypeScript.

### Uso de interfaces en funciones

En TypeScript, el uso de interfaces en funciones proporciona
una forma efectiva de especificar el tipo de los parámetros y
el tipo de retorno que la función debe aceptar y devolver.
Observa el siguiente ejemplo:

```ts
// Definición de una interfaz para estructurar objetos
interface Punto {
    x: number;
    y: number;
}

// Definición de una interfaz para la función
interface CalculadoraDistancia {
    calcularDistancia(p1: Punto, p2: Punto): number;
}

// Implementación de la interfaz en una función
const calculadora: CalculadoraDistancia = {
    calcularDistancia(p1: Punto, p2: Punto): number {
        const distanciaX = p2.x - p1.x;
        const distanciaY = p2.y - p1.y;
        return Math.sqrt(distanciaX ** 2 + distanciaY ** 2);
    }
};

// Uso de la función
const puntoA: Punto = { x: 1, y: 2 };
const puntoB: Punto = { x: 4, y: 6 };

const distancia: number = calculadora.calcularDistancia(puntoA, puntoB);
console.log(`La distancia entre los puntos es: ${distancia}`);
```

En este ejemplo:

- Se define una interfaz **Punto** para estructurar objetos que
representan coordenadas x e y.
- Se define la interfaz **CalculadoraDistancia** que especifica
una función llamada **calcularDistancia** que toma dos puntos
(**Punto**) como parámetros y devuelve un número.
- Se implementa la interfaz en un objeto **calculadora**,
que tiene una función **calcularDistancia**.
- Se utilizan objetos que cumplen con la interfaz **Punto** para representar puntos.
- Se llama a la función **calcularDistancia** utilizando el objeto **calculadora** para obtener la distancia entre dos puntos.

Este enfoque facilita el mantenimiento del código al proporcionar
una estructura clara y permitir la verificación de tipos en
funciones específicas.
