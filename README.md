# Introducción a TypeScript

Descubre el poder de TypeScript en el desarrollo web.
Este superset de JavaScript mejora proyectos,
elevando la calidad del código. En esta introducción,
proporcionaremos una base sólida para aprovechar
al máximo las capacidades de TypeScript.
¡Bienvenida al mundo de TypeScript!

## Contenido

- [¿Que es TypeScript?](#¿que-es-typescript)
- [Descubriendo las ventajas de TypeScript](#descubriendo-las-ventajas-de-typescript)
- [Ejemplos prácticos: de la teoria a la realidad del codigo](#ejemplos-practicos-de-la-teoria-a-la-realidad-del-codigo)
- [Diferencias entre JavaScript y TypeScript](#diferencias-entre-javascript-y-typescript)
- [Creando un archivo .js a traves de un  archivo de TypeScript](#creando-un-archivo-js-a-traves-de-un-archivo-de-typescript)
- [Siguientes pasos](#siguientes-pasos)
- [Conclusion](#conclusion)

### ¿Que es TypeScript?

TypeScript se presenta como un superset de
JavaScript, lo que significa que amplía las
capacidades de JavaScript al agregar mejoras y
características. En esencia, puedes pensar en
TypeScript como JavaScript con "superpoderes",
principalmente debido a su capacidad para trabajar con
tipos de datos de manera más explícita.

> [!NOTE]
> En matemáticas, un superset es un conjunto que
> contiene todos los elementos de otro conjunto.
> En el caso de TypeScript, es un superset de
> JavaScript. Esto significa que todo lo que puedes
> hacer en JavaScript, también puedes hacerlo en
> TypeScript.

### Descubriendo las ventajas de typeScript

- Detección de errores más fácil:
Sistema de tipado estático detecta errores,
brinda detección temprana y mejora la calidad
del código.

- Mantenimiento sencillo a largo plazo: La
tipificación explícita facilita el mantenimiento
en proyectos extensos, aumenta claridad y reduce
errores potenciales.

- Integración precisa con el IDE: Integración
fluida con IDE brinda sugerencias precisas,
agilizando la escritura de código y mejorando
productividad.

- Código robusto, confiable y documentado:
Tipificación estática y estructura clara
fomentan código sólido, confiable y fácilmente
documentable, facilitando colaboración entre
desarrolladoras.

- Versatilidad en el desarrollo: Compatible
con Frontend, Backend y desarrollo móvil,
posibilitando aplicaciones versátiles en
diversas áreas del desarrollo web.

### Ejemplos practicos: de la teoria a la realidad del codigo

Observa el siguiente ejemplo:

```js
function compact(arr) {
    if (orr.length > 10)
     return arr.trim(0, 10)
    return arr
}
```

- En ocasiones es difícil encontrar el error hasta no ejecutar el código
- Es difícil de predecir exactamente que esperamos con `arr` porque el nombre `arr` se puede interpretar que se espera
un arreglo sin embardo tenemos que terminar
de leer la función completa para saber tipo de
dato espera `arr`
- El código no esta documentado
- Si pasamos un arreglo como argumento esta función no podría trabajar porque el método `trim` trabaja con un string y se
encarga de borra los espacios de un lado

Ahora veamos el siguiente código:

```ts
function compact(arr: string[]) {
  if (arr.length > 10)
    return arr.slice(0, 10)
  return arr
}
```

- A diferencia del código anterior podemos observar que especificamos el tipo de dato de `arr` lo cual nos permitirá
agregar cambios en el futuro.
- Por otro lado es legible el código y no cambia la forma en como se percibe la funcionalidad
- Se establece que el parámetro `arr` es de tipo *arreglo* compuesto de *strings*

#### Ejemplo de tipos y tipados

> [!IMPORTANT]
> Documentación sobre [tipos de datos](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html)

| Type | Predicate |
|---|---|
|string| typeof s === "string"|
| number | typeof n === "number" |
| boolean | typeof b === "boolean" |
| undefined | typeof undefined === "undefined" |
| function | typeof f === "function" |
| array | Array.isArray(a) |

```ts
let name: string = "Ejemplo";
let age: number = 25;
let isActive: boolean = true;
```

#### Ejemplos de tipado en funciones

> [!TIP]
> [Prueba el código del ejemplo aquí](https://www.TypeScriptlang.org/play)

##### Paso 1

```ts
// Vamos a crear un objeto donde tendremos name: string y id: number
const userObject = {
  name: "Hayes",
  id: 0,
};
```

##### Paso 2

```ts
// Ahora puedes especificar explícitamente la forma de este objeto usando una declaración de interface:
interface UserInterface {
  name: string; // Aquí especificamos que name sera de tipo string
  id: number; // Aquí especificamos que id es de tipo number
}
```

##### Paso 3

###### Usar el tipado en funciones para especificar la forma de un parámetro

```ts
// Ahora puedes declarar que un una función donde el parámetro esperado se ajusta a la forma de tu interfaz
function printUser(user: UserInterface) {
  return 'Hello '+user.name;
}
console.log(printUser(userObject));
```

###### Usar el tipado en funciones para especificar la forma en que retornara un valor la función

```ts
// Ahora puedes declarar que un una función donde el parámetro esperado se ajusta a la forma de tu interfaz
function getUser(): UserInterface { // En seguida de los paréntesis podemos especificar como sera el retorno.
  return userObject;
}
console.log(getUser());
```

### Diferencias entre JavaScript y TypeScript

Este código JavaScript suma dos números y devuelve el resultado.

```js
function add(a, b) {
  return a + b;
}

const sum = add(1, 2); // 3
```

Este código TypeScript hace lo mismo que el código JavaScript,
pero especifica los tipos de datos de los argumentos `a` y `b` como `number`.
Esto ayuda a prevenir errores en tiempo de ejecución, ya que TypeScript
garantizará que solo se puedan pasar números a la función `add()`.

```ts
function add(a: number, b: number) {
  return a + b;
}

const sum = add(1, 2); // 3
```

El siguiente código JavaScript crea un objeto `user` con dos propiedades: `name` y `age`.
Luego, la variable `greeting` se usa para imprimir una cadena de saludo
que incluye el nombre del usuario.

```js
const user = {
  name: "John Doe",
  age: 30,
};

const greeting = `Hola, ${user.name}!`;
```

El siguiente código TypeScript hace lo mismo que el código JavaScript,
pero define una interfaz llamada `User` que especifica los tipos
de datos de las propiedades `name` y `age`. Esto ayuda a prevenir
errores en tiempo de ejecución, ya que TypeScript garantizará
que el objeto user cumpla con la interfaz `User`.

```ts
interface User {
  name: string;
  age: number;
}

const user: User = {
  name: "John Doe",
  age: 30,
};

const greeting = `Hola, ${user.name}!`; // Hola, John Doe!
```

En general, las principales diferencias entre JavaScript y TypeScript son las siguientes:

- TypeScript es un lenguaje de tipado estático, mientras que JavaScript es un lenguaje de tipado dinámico.
  - Esto significa que TypeScript requiere que los tipos de datos se especifiquen explícitamente, mientras que JavaScript permite que los tipos de datos se infieran de la asignación de valores.

- TypeScript tiene una sintaxis más expresiva que JavaScript.
  - Por ejemplo, TypeScript permite usar interfaces para definir los tipos de datos de los objetos.

### Creando un archivo .js a traves de un  archivo de TypeScript

Para este ejemplo se requiere instalar TypeScript en tu computadora de forma global (recuerda que TypeScript no se ejecuta... Se transpila), para eso usaremos la siguiente linea de código.

```bash
npm install -g typescript
```

Ahora nos toca crear un archivo nuevo llamado **Hello.ts** y ábrelo con tu editor de código y escribe lo siguiente:

```ts
function greet(person: string, date: Date) {
  console.log(`Hi ${person}, today is ${date.toDateString()}!`);
}

greet("Maddison", new Date());

```

Ahora en la misma raíz donde guardaste el archivo **Hello.ts** ejecuta el siguiente comando:

```bash
tsc -w Hello.ts
```

Como resultado se debió haber creado un nuevo archivo llamado **Hello.js** y el código que contiene es muy similar (pero
no igual) al archivo  **Hello.ts** la diferencia es que el archivo **Hello.js** lo puedes usar para ser ejecutado.

### Siguientes pasos

- [Resvisa el manual de la documentación oficial](https://www.typescriptlang.org/docs/handbook/intro.html)
- [Puedes generar el archivo tsconfig.json](https://www.typescriptlang.org/docs/handbook/compiler-options.html)
- [Angular trabaja nativamente con TS](https://angular.io/guide/typescript-configuration)
- [Node con typescript](https://nodejs.org/en/learn/getting-started/nodejs-with-typescript)
- [React con TS](https://es.react.dev/learn/typescript)
- [Learn TypeScript](https://www.tutorialsteacher.com/typescript)

### Conclusion

TypeScript ha evolucionado mucho, hoy en dia es muy popular y su capacidad para añadir tipos estáticos a JavaScript no
solo brinda una capa adicional de seguridad y detección de errores, sino que también impulsa la productividad y la
escalabilidad de los proyectos. Al aprender TypeScript, te sumerges en un ecosistema que fomenta la creación de código
más limpio, legible y mantenible, si tienes alguna duda no olvides: usar ExplainDev, usar los canales de los proyecto,
preguntarle a tus coaches, asistir a git-camp y test-camp, esperamos que esta Introducción a TypeScript te sea de utilidad.
