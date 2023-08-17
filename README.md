### Tutorial de programación con javascript

##### A continuacion realizaremos la explicación de varios ejercicios de programación con javascript:

Tenemos 4 variables declaradas y asignadas con su valor fijo, y el console.log solo nos puede imprimir esta informacion. 
```
const name = "Ivonne";
const lastName = "Moreno";
const completeName = name + lastname;
const nickName = "Bombon";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
```

Con la función podremos asignarle el valor que querramos a las variables que solo fueron declaradas mas no asignadas hasta no mandar llamar la función.
```
//Cambio a función
function presentation(name, lastName, nickName){
  return console.log(`Mi nombre completo es ${name} ${lastName}, pero prefiero que me digas ${nickName}.`);
}

presentation("Ivonne", "Moreno", "Bombon");
```

#### A continuación veremos el cambio de una condicional switch a if

Un condicional en programación es una estructura que permite ejecutar diferentes bloques de código en función de una condición o expresión booleana. En otras palabras, los condicionales permiten que el flujo del programa tome decisiones basadas en ciertas condiciones.

```
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
case "Free":
       console.log("Solo puedes tomar los cursos gratis");
break;
case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
break;
case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
break;
case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
break;
}

//Cambio de condicional
const tipoDeSuscripcion = "Basic";

if (tipoDeSuscripcion == "Free") {
	console.log("Solo puedes tomar los cursos gratis");
} else if (tipoDeSuscripcion == "Basic") {
	 console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if (tipoDeSuscripcion == "Expert") {
	 console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else if (tipoDeSuscripcion == "ExpertPlus") {
	 console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
} else {
	 console.log("No tienes ninguna suscripción");
}
```

#### Ahora veremos los ciclos

Un ciclo en programación es una estructura que permite repetir un bloque de código varias veces hasta que se cumpla una condición específica. Los ciclos son útiles para automatizar tareas repetitivas y para procesar una serie de elementos de manera eficiente.

En JavaScript, existen principalmente tres tipos de ciclos: `for`, `while` y `do-while`. A continuación, te explico cada uno de ellos:

1. **for**: El ciclo `for` se utiliza para repetir un bloque de código un número específico de veces. Se compone de tres partes: la inicialización, la condición y la actualización. Ejemplo:

```javascript
for (inicialización; condición; actualización) {
    // Código a repetir
}
```

2. **while**: El ciclo `while` se ejecuta mientras una condición sea verdadera. La condición se verifica antes de cada iteración. Ejemplo:

```javascript
while (condición) {
    // Código a repetir mientras la condición sea verdadera
}
```

3. **do-while**: El ciclo `do-while` es similar al ciclo `while`, pero se asegura de que el bloque de código se ejecute al menos una vez antes de verificar la condición. Ejemplo:

```javascript
do {
    // Código a repetir al menos una vez
} while (condición);
```

Un ciclo infinito es un ciclo que nunca se detiene debido a una condición que siempre es verdadera. Esto puede ser un problema grave, ya que hará que el programa se quede ejecutando indefinidamente y puede causar que el sistema se bloquee o se vuelva inaccesible. Los ciclos infinitos son considerados errores y deben evitarse a toda costa.

Sí, puedes mezclar ciclos y condicionales en JavaScript. De hecho, esta combinación es muy común y poderosa. Puedes usar ciclos para repetir un bloque de código y dentro de ese bloque, puedes utilizar condicionales para tomar decisiones basadas en ciertas condiciones. Por ejemplo:

```javascript
for (let i = 1; i <= 10; i++) {
    if (i % 2 === 0) {
        console.log(i + " es par");
    } else {
        console.log(i + " es impar");
    }
}
```

En este ejemplo, estamos utilizando un ciclo `for` para iterar del 1 al 10, y dentro del ciclo, estamos usando un condicional para determinar si cada número es par o impar.

#### Usar prompt


```
let respuesta;

do {
    respuesta = prompt("¿Cuánto es 2 + 2?");
    
    if (respuesta === "4") {
        console.log("¡Felicitaciones! ¡Respuesta correcta!");
    } else {
        console.log("Respuesta incorrecta. Inténtalo de nuevo.");
    }
} while (respuesta !== "4");

```
En este código, el ciclo do-while se ejecuta mientras la respuesta del usuario no sea igual a "4". Si el usuario ingresa "4", se muestra un mensaje de felicitaciones y el ciclo se detiene. Si el usuario ingresa una respuesta incorrecta, se muestra un mensaje de error y el ciclo se repite para darle otra oportunidad de responder correctamente.

#### Continuemos con los arrays

Un array es una estructura de datos que permite almacenar múltiples valores en una sola variable. Estos valores pueden ser de cualquier tipo, como números, cadenas de texto, objetos, otros arrays, entre otros. Los elementos en un array están ordenados y se acceden mediante un índice numérico que comienza desde cero.

```
const numeros = [1, 2, 3, 4, 5];
const colores = ["rojo", "verde", "azul"];
```

#### ¿Que es un objeto?

Un objeto es una colección de propiedades, donde cada propiedad tiene un nombre y un valor asociado. En lugar de acceder a los elementos a través de índices numéricos como en los arrays, en los objetos se accede a las propiedades utilizando sus nombres. Los objetos son útiles para representar entidades más complejas con múltiples características.

```
const persona = {
    nombre: "Juan",
    edad: 30,
    ocupacion: "programador"
};
```

###### Cuándo usar objetos o arrays:
La elección entre usar objetos o arrays depende del contexto y de los datos que necesites representar:
**Arrays:** Son útiles cuando tienes una lista de elementos del mismo tipo, como una lista de números, nombres o colores. Se utilizan para almacenar colecciones ordenadas de datos.

**Objetos:** Son ideales cuando necesitas representar una entidad con propiedades que tienen nombres significativos, como un usuario con nombre, edad y dirección. Los objetos son más expresivos para representar datos más complejos y estructurados.

**Combinar arrays y objetos:**
Sí, puedes mezclar arrays y objetos en JavaScript, incluso en estructuras más complejas. Por ejemplo, podrías tener un array de objetos o un objeto que contenga arrays como propiedades. Esto te permite manejar datos más diversos y organizados.

**Ejemplo de un array de objetos:**
```
const personas = [
    { nombre: "Ana", edad: 25 },
    { nombre: "Luis", edad: 32 },
    { nombre: "María", edad: 28 }
];
```

**Ejemplo de un objeto con arrays como propiedades:**
```
const datos = {
    numeros: [1, 2, 3],
    colores: ["rojo", "verde", "azul"]
};
```

En resumen, arrays y objetos son dos tipos de estructuras fundamentales en JavaScript que te permiten manejar diferentes tipos de datos de manera efectiva y flexible.

#### Ahora crearemos una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.
```
function imprimirPrimerElemento(arr) {
    if (Array.isArray(arr) && arr.length > 0) {
        console.log("El primer elemento del array es:", arr[0]);
    } else {
        console.log("El parámetro no es un array válido o está vacío.");
    }
}

// Ejemplos de uso
const numeros = [1, 2, 3, 4, 5];
const colores = ["rojo", "verde", "azul"];

imprimirPrimerElemento(numeros); // Salida: El primer elemento del array es: 1
imprimirPrimerElemento(colores); // Salida: El primer elemento del array es: rojo
imprimirPrimerElemento([]); // Salida: El parámetro no es un array válido o está vacío.
```

#### Crearemos una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

Esta función imprimirElementos verifica si el parámetro recibido es un array válido y tiene al menos un elemento antes de recorrer el array y mostrar cada elemento por separado en la consola.

```
function imprimirElementos(arr) {
    if (Array.isArray(arr) && arr.length > 0) {
        console.log("Elementos del array:");
        for (let i = 0; i < arr.length; i++) {
            console.log(arr[i]);
        }
    } else {
        console.log("El parámetro no es un array válido o está vacío.");
    }
}

// Ejemplos de uso
const numeros = [1, 2, 3, 4, 5];
const colores = ["rojo", "verde", "azul"];

imprimirElementos(numeros);
// Salida:
// Elementos del array:
// 1
// 2
// 3
// 4
// 5

imprimirElementos(colores);
// Salida:
// Elementos del array:
// rojo
// verde
// azul

imprimirElementos([]);
// Salida: El parámetro no es un array válido o está vacío.
```

#### Ahora crearemos una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

Esta función **imprimirPropiedades** verifica si el parámetro recibido es un objeto válido antes de recorrer las propiedades del objeto y mostrar cada propiedad y su valor en la consola.

```
function imprimirPropiedades(obj) {
    if (typeof obj === "object" && obj !== null) {
        console.log("Propiedades del objeto:");
        for (const key in obj) {
            if (obj.hasOwnProperty(key)) {
                console.log(`${key}: ${obj[key]}`);
            }
        }
    } else {
        console.log("El parámetro no es un objeto válido.");
    }
}

// Ejemplo de uso
const persona = {
    nombre: "Ivonne",
    edad: 30,
    ocupacion: "programador"
};

imprimirPropiedades(persona);
// Salida:
// Propiedades del objeto:
// nombre: Ivonne
// edad: 30
// ocupacion: programador
```
#### Ejercicio de palindromos
**Con un ciclo**
```
function esPalindromo(cadena) {
  const cleanedCadena = cadena.replace(/\s/g, '').toLowerCase();
  const longitud = cleanedCadena.length;

  for (let i = 0; i < longitud / 2; i++) {
    if (cleanedCadena[i] !== cleanedCadena[longitud - 1 - i]) {
      return false;
    }
  }
  return true;
}

const palabraOfrase = prompt("Ingrese una palabra o frase:");
if (esPalindromo(palabraOfrase)) {
  console.log("Es un palíndromo.");
} else {
  console.log("No es un palíndromo.");
}
```

**sin el ciclo con una funcion y condicional**
```
function verificarPalindromo(cadena) {
  const cleanedCadena = cadena.replace(/\s/g, '').toLowerCase();
  const reversedCadena = cleanedCadena.split('').reverse().join('');

  if (cleanedCadena === reversedCadena) {
    return "Es un palíndromo.";
  } else {
    return "No es un palíndromo.";
  }
}

const palabraOfrase = prompt("Ingrese una palabra o frase:");
const resultado = verificarPalindromo(palabraOfrase);
console.log(resultado);
```
