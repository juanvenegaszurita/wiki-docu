# Indice

- [Javascript](#javascript)
  - [Conceptos Básicos](#conceptosBasicos)
    - [Bloque](#bloque)
      - [Ejemplo (Bloque)](#ejemploBloque)
    - [Declaración de variables](#declaraciondeVariables)
    - [Tipos de datos](#tiposDeDatos)
      - [Ejemplo (Tipos de datos)](#ejemploTiposdeDatos)
  - [Bucles](#bucles)
    - [while](#while)
      - [Sintaxis while](#sintaxisWhile)
      - [Ejemplo (while)](#ejemploWhile)
    - [do...while](#doWhile)
      - [Sintaxis do...while](#sintaxisDoWhile)
      - [Ejemplo (do...while)](#ejemploDoWhile)
    - [for](#for)
      - [Sintaxis for](#sintaxisFor)
      - [Ejemplo (for)](#ejemploFor)
  - [Condicionales](#condicionales)
    - [if else](#ifElse)
      - [Sintaxis if else](#sintaxisIfElse)
      - [Ejemplo (if else)](#ejemploIfElse)
    - [switch](#switch)
      - [Sintaxis switch](#sintaxisSwitch)
      - [Ejemplo (switch)](#ejemploSwitch)
  - [Operadores de asignación](#operadoresDeAsignacion)
  - [Operadores de comparación](#operadoresDeComparacion)
  - [Funciones](#funciones)
    - [function*](#functionn)
      - [Sintaxis function*](#sintaxisFunctionn)
      - [Ejemplo (function*)](#ejemploFunctionn)
    - [function](#functiona)
      - [Sintaxis function](#sintaxisFunction)
      - [Ejemplo (function)](#ejemploFunction)
    - [Funciones Flecha](#funcionesFlecha)
      - [Sintaxis Funciones Flecha](#sintaxisFuncionesFlecha)
      - [Ejemplo (Funciones Flecha)](#ejemploFuncionesFlecha)
- [Ejemplo de lo aprendido](#ejemploDeLoAprendido)

<div id='javascript'>

# Javascript

<div id='conceptosBasicos'>

## Conceptos Básicos

<div id='Bloque'>

### Bloque

Una sentencia block se utiliza para agrupar cero o más sentencias. Este grupo block se delimita por un par de llaves.

<div id='ejemploBloque'>

#### Ejemplo (Bloque)

```javascript
{
  sentencia_1;
  sentencia_2;
  sentencia_n;
}
```

<div id='declaraciondeVariables'>

### Declaración de variables

JavaScript tiene tres tipos de declaraciones de variables.

- **var** Declara una variable, opcionalmente la inicia a un valor.

  ```javascript
  var variable_var = 0;
  ```

- **let** Declara una variable local con ámbito de [bloque](#bloque), opcionalmente la inicia a un valor.

  correcto

  ```javascript
  let variable_let = 0;
  console.log(variable_let)
  ```

  incorrecto

  ```javascript
  {
    let variable_let = 0;
  }
  console.log(variable_let)
  ```

- **const** Declara un nombre de constante de solo lectura y ámbito de [bloque](#bloque).

  correcto

  ```javascript
  const variable_const = 0;
  console.log(variable_const)
  ```

  incorrecto

  ```javascript
  {
    const variable_const = 0;
    console.log(variable_const)
    // esto causa un error ya que es solo lectura
    variable_const = 3;
  }
  ```

<div id='tiposDeDatos'>

### Tipos de datos

1. **Boolean**: true y false
2. **null**: Una palabra clave especial que denota un valor nulo. (Dado que JavaScript distingue entre mayúsculas y minúsculas, null no es lo mismo que Null, NULL o cualquier otra variante).
3. **undefined**: Una propiedad de alto nivel cuyo valor no está definido.
4. **Number**: Un número entero o un número con coma flotante. Por ejemplo: 42 o 3.14159.
5. **BigInt**: Un número entero con precisión arbitraria. Por ejemplo: 9007199254740992n.
6. **String**: Una secuencia de caracteres que representan un valor de texto. Por ejemplo: "Hola"
7. **Symbol**: (nuevo en ECMAScript 2015). Un tipo de dato cuyas instancias son únicas e inmutables

<div id='ejemploTiposdeDatos'>

#### Ejemplo (Tipos de datos)

```javascript
// Boolean
const verdadero = true;
const falso = false;

// null
const nulo = null;

// undefined
const indefinido = undefined;

// number
const numerico = 50;

// BigInt
const numero_grande = 446468484464646n;

// String
const texto_comillas_dobles = "Comillas simples.";
const texto_comillas_simple = 'Comillas dobles.';
const texto_concatenado = "hola "+texto_comillas_dobles+" "+texto_comillas_simple;
// String - Plantillas literales (plantillas de cadenas)
const plantilla_literal = `Este es un
texto en donde puedes
agregar saltos de líneas y puedes concatenar así : ${texto_concatenado}`;
```

<div id='bucles'>

## Bucles

<div id='while'>

### while

Crea un bucle que ejecuta una sentencia especificada mientras cierta condición se evalúe como verdadera. Dicha condición es evaluada antes de ejecutar la sentencia

<div id='sintaxisWhile'>

#### Sintaxis while

```text
while (condicion)
  sentencia
```

- **consdición**

    Una expresión que se evalúa antes de cada paso del bucle. Si esta condición se evalúa como verdadera, se ejecuta sentencia. Cuando la condición se evalúa como false, la ejecución continúa con la sentencia posterior al bucle while.

- **sentencia**

    Una sentecia que se ejecuta mientras la condición se evalúa como verdadera. Para ejecutar múltiples sentencias dentro de un bucle, utiliza una sentencia [bloqueb(#Bloque) para agrupar esas sentencias.

<div id='ejemploWhile'>

#### Ejemplo (while)

```javascript
n = 0;
x = 0;
while (n < 3) {
  n ++;
  x += n;
  console.log("Valor de n : "+n+" Valor de x :"+x)
}
/*
Salida
Valor de n : 1 Valor de x :1
Valor de n : 2 Valor de x :3
Valor de n : 3 Valor de x :6
*/
```

<div id='doWhile'>

### do...while

La sentencia (hacer mientras) crea un bucle que ejecuta una sentencia especificada, hasta que la condición de comprobación se evalúa como falsa. La condición se evalúa después de ejecutar la sentencia, dando como resultado que la sentencia especificada se ejecute al menos una vez.

<div id='sintaxisDoWhile'>

#### Sintaxis do...while

```text
do
   sentencia
while (condición);
```

- **sentencia**

    Una sentencia que se ejecuta al menos una vez y es reejecutada cada vez que la condición se evalúa a verdadera. Para ejecutar múltiples sentencias dentro de un bucle, utilice la sentencia [bloqueb(#Bloque) para agrupar aquellas sentencias.
  
- **consdición**

    Una expresión se evalúa después de cada pase del bucle. Si condición se evalúa como verdadera, la sentencia se re-ejecuta. Cuando condición se evalúa como falsa, el control pasa a la siguiente sentencia hacer mientras.

<div id='ejemploDoWhile'>

#### Ejemplo (do...while)

```javascript
let i = 0;
do {
   i += 1;
   console.log("Valor de i: "+i);
} while (i < 5);
/*
Salida
Valor de i: 1
Valor de i: 2
Valor de i: 3
Valor de i: 4
Valor de i: 5
*/
```

<div id='for'>

### for

Crea un bucle que consiste en tres expresiones opcionales, encerradas en paréntesis y separadas por puntos y comas, seguidas de una sentencia ejecutada en un bucle.

<div id='sintaxisFor'>

#### Sintaxis for

```text
for ([expresion-inicial]; [condicion]; [expresion-final])sentencia
```

- **expresion-inicial**

    Una expresión (incluyendo las expresiones de asignación) o la declaración de variable. Típicamente se utiliza para usarse como variable contador. Esta expresión puede opcionalmente declarar nuevas variables con la palabra clave var. Estas variables no son locales del bucle, es decir, están en el mismo alcance en el que está el bucle for. El resultado de esta expresión es descartado.

- **condicion**

    Una expresión para ser evaluada antes de cada iteración del bucle. Si esta expresión se evalúa como verdadera, se ejecuta sentencia. Esta comprobación condicional es opcional. Si se omite, la condición siempre se evalúa como verdadera. Si la expresión se evalúa como falsa, la ejecución salta a la primera expresión que sigue al constructor de for.

- **expresion-final**

    Una expresión para ser evaluada al final de cada iteración del bucle. Esto ocurre antes de la siguiente evaluación de la condicion. Generalmente se usa para actualizar o incrementar la variable contador.

- **sentencia**

    Una sentencia que se ejecuta mientras la condición se evalúa como verdadera. Para ejecutar múltiples sentencias dentro del bucle, utilice una sentencia [bloqueb(#Bloque) para agrupar aquellas sentecias.

<div id='ejemploFor'>

#### Ejemplo (for)

```javascript
let n = 0
for (var i = 0; i < 9; i++) {
   n += i;
   console.log("Valor de n :"+n);
}
/*
Salida
Valor de n :0
Valor de n :1
Valor de n :3
Valor de n :6
Valor de n :10
Valor de n :15
Valor de n :21
Valor de n :28
Valor de n :36
*/
```
<div id='condicionales'>

## Condicionales

<div id='ifElse'>

### if else

Ejecuta una sentencia si una condición específicada es evaluada como verdadera. Si la condición es evaluada como falsa, otra sentencia puede ser ejecutada.

<div id='sintaxisIfElse'>

#### Sintaxis if else

```text
if (condición) sentencia1 [else sentencia2]
```

- **condición**

    Una expresión que puede ser evaluada como verdadera o falsa.

- **sentencia1**

    Sentencia que se ejecutará si condición es evaluada como verdadera. Puede ser cualquier sentencia, incluyendo otras sentenccias if anidadas. Para ejecutar múltiples sentencias, use una sentencia [bloqueb(#Bloque) para agruparlas.

- **sentencia2**

    Sentencia que se ejecutará si condición se evalúa como falsa, y exista una cláusula else. Puede ser cualquier sentencia, incluyendo sentencias block y otras sentencias if anidadas.

<div id='ejemploIfElse'>

#### Ejemplo (if else)

```javascript
// solo if
const edad = 18;
if( edad >= 18 ) {
  console.log("Es mayor de edad")
}

// if else
const edad = 16;
if( edad < 18 ) {
  console.log("Es menor de edad")
} else {
  console.log("Es mayor de edad")
}

// Múltiples else if 
const edad = 65;
if( edad < 18 ) {
  console.log("Es menor de edad")
} else if ( edad >=18 && edad < 65 ){
  console.log("Es mayor de edad")
} else {
  console.log("Es de tercera edad")
}
```

<div id='switch'>

### switch

La declaración switch evalúa una expresión, comparando el valor de esa expresión con una instancia case, y ejecuta declaraciones asociadas a ese case, así como las declaraciones en los case que siguen.

<div id='sintaxisSwitch'>

#### Sintaxis switch

```text
switch (expresión) {
  case valor1:
    //Declaraciones ejecutadas cuando el resultado de expresión coincide con el valor1
    [break;]
  case valor2:
    //Declaraciones ejecutadas cuando el resultado de expresión coincide con el valor2
    [break;]
  ...
  case valorN:
    //Declaraciones ejecutadas cuando el resultado de expresión coincide con valorN
    [break;]
  default:
    //Declaraciones ejecutadas cuando ninguno de los valores coincide con el valor de la expresión
    [break;]
}
```

- **expresión**

    Es una expresión que es comparada con el valor de cada instancia case.

- **case valorN**

    Una instancia case valorN es usada para ser comparada con la expresión. Si la expresión coincide con el valorN, las declaraciones dentro de la instancia case se ejecutan hasta que se encuentre el final de la declaración switch o hasta encontrar una interrupción break.

- **default**

    Una instancia default, cuando es declarada, es ejecutada si el valor de la expresión no coincide con cualquiera de las otras instancias case valorN.

<div id='ejemploSwitch'>

#### Ejemplo (switch)

```javascript
const fruta = 'Naranjas'
switch (fruta) {
  case 'Naranjas':
    console.log('El kilogramo de naranjas cuesta $0.59.');
    break;
  case 'Manzanas':
    console.log('El kilogramo de manzanas cuesta $0.32.');
    break;
  case 'Platanos':
    console.log('El kilogramo de platanos cuesta $0.48.');
    break;
  case 'Cerezas':
    console.log('El kilogramo de cerezas cuesta $3.00.');
    break;
  case 'Mangos':
  case 'Papayas':
    console.log('El kilogramo de mangos y papayas cuesta $2.79.');
    break;
  default:
    console.log('Lo lamentamos, por el momento no disponemos de ' + fruta + '.');
}

/*
Salida
El kilogramo de naranjas cuesta $0.59.
*/
```

<div id='operadoresDeAsignacion'>

## Operadores de asignación

Un operador de asignación asigna un valor a su operando izquierdo basándose en el valor de su operando derecho. El operador de asignación simple es igual (=), que asigna el valor de su operando derecho a su operando izquierdo. Es decir, x = y asigna el valor de y a x.

También hay operadores de asignación compuestos que son una abreviatura de las operaciones enumeradas en la siguiente tabla:

| Nombre | Operador abreviado | Significado |
|---|---|---|
| Asignación | x = y | x = y |
| Asignación de adición | x += y | x = x + y |
| Asignación de resta | x -= y | x = x - y |
| Asignación de multiplicación | x *= y | x = x * y |
| Asignación de división | x /= y | x = x / y |
| Asignación de residuo | x %= y | x = x % y |
| Asignación de exponenciación | x **= y | x = x ** y |
| Asignación de desplazamiento a la izquierda | x <<= y | x = x << y |
| Asignación de desplazamiento a la derecha | x >>= y | x = x >> y |
| Asignación de desplazamiento a la derecha sin signo | x >>>= y | x = x >>> y |
| Asignación AND bit a bit | x &= y | x = x & y |
| Asignación XOR bit a bit | x ^= y | x = x ^ y |
| Asignación OR bit a bit | x |= y | x = x | y |
| Asignación AND lógico | x &&= y | x && (x = y) |
| Asignación OR lógico | x ||= y | x || (x = y) |
| Asignación de anulación lógica | 	x ??= y | x ?? (x = y) |

<div id='operadoresDeComparacion'>

## Operadores de comparación

Un operador de comparación compara sus operandos y devuelve un valor lógico en función de si la comparación es verdadera (true) o falsa (false). Los operandos pueden ser valores numéricos, de cadena, lógicos u objetos. Las cadenas se comparan según el orden lexicográfico estándar, utilizando valores Unicode. En la mayoría de los casos, si los dos operandos no son del mismo tipo, JavaScript intenta convertirlos a un tipo apropiado para la comparación. Este comportamiento generalmente resulta en comparar los operandos numéricamente. Las únicas excepciones a la conversión de tipos dentro de las comparaciones involucran a los operadores === y !==, que realizan comparaciones estrictas de igualdad y desigualdad. Estos operadores no intentan convertir los operandos a tipos compatibles antes de verificar la igualdad. La siguiente tabla describe los operadores de comparación en términos de este código de ejemplo:

```text
var var1 = 3;
var var2 = 4;
```

| Operador | Descripción | Ejemplos que devuelven true |
|---|---|---|
| Igual (==) | Devuelve true si los operandos son iguales. |  3 == var1<br>"3" == var1<br>3 == '3'|
| No es igual (!=) | Devuelve true si los operandos no son iguales. | var1 != 4<br>var2 != "3" |
| Estrictamente igual (===) | Devuelve true si los operandos son iguales y del mismo tipo. Consulta también Object.is y similitud en JS. | 3 === var1 |
| Desigualdad estricta (!==) | Devuelve true si los operandos son del mismo tipo pero no iguales, o son de diferente tipo. | var1 !== "3"<br>3 !== '3' |
| Mayor que (>) | Devuelve true si el operando izquierdo es mayor que el operando derecho. | var2 > var1<br>"12" > 2 |
| Mayor o igual que (>=) | Devuelve true si el operando izquierdo es mayor o igual que el operando derecho. | var2 >= var1<br>var1 >= 3 |
| Menor que (<) | Devuelve true si el operando izquierdo es menor que el operando derecho. | var1 < var2<br>"2" < 12 |
| Menor o igual (<=) | Devuelve true si el operando izquierdo es menor o igual que el operando derecho. | var1 <= var2<br>var2 <= 5 |

<div id='funciones'>

## Funciones

<div id='functionn'>

### function*

La declaración function* (la palabra clave function seguida de un asterisco) define una función generadora, que devuelve un objeto Generator.

<div id='sintaxisFunctionn'>

#### Sintaxis function*

```text
function* nombre([param[, param[, ... param]]]) {
   instrucciones
}
```

- **nombre**

    El nombre de la función.

- **param**

    El nombre de los argumentos que se le van a pasar a la función. Una función puede tener hasta 255 argumentos.

- **instrucciones**

    Las instrucciones que componen el cuerpo de la función.

<div id='ejemploFunctionn'>

#### Ejemplo (function*)

```javascript
// Ejemplo simple
function* idMaker(){
  var index = 0;
  while(index < 3)
    yield index++;
}

var gen = idMaker();

console.log(gen.next().value); // 0
console.log(gen.next().value); // 1
console.log(gen.next().value); // 2
console.log(gen.next().value); // undefined

// Ejemplo con yield*
function* anotherGenerator(i) {
  yield i + 1;
  yield i + 2;
  yield i + 3;
}

function* generator(i){
  yield i;
  yield* anotherGenerator(i);
  yield i + 10;
}

var gen = generator(10);

console.log(gen.next().value); // 10
console.log(gen.next().value); // 11
console.log(gen.next().value); // 12
console.log(gen.next().value); // 13
console.log(gen.next().value); // 20
```

<div id='functiona'>

### function

Declara una función con los parámetros especificados.

Puede también definir funciones usando el constructor Function y el function (expresión function).

<div id='sintaxisFunction'>

#### Sintaxis function

```text
function nombre([parametro1] [,parametro2] [..., parametroN]) {sentencias}
```

- **nombre**

    El nombre de la función.

- **parametroN**

  El nombre de un argumento que se pasa a la función. Una función puede tener hasta 255 argumentos.

- **sentencias**

  Las sentencias que comprenden el cuerpo de la función.

<div id='ejemploFunction'>

#### Ejemplo (function)

```javascript
function calcular_ventas(unidades_a, unidades_b, unidades_c) {
   return unidades_a*79 + unidades_b * 129 + unidades_c * 699;
}
console.log( calcular_ventas(10,50,30))
/*
Salida
28210
*/
```

<div id='funcionesFlecha'>

### Funciones Flecha

Una expresión de función flecha es una alternativa compacta a una expresión de función tradicional, pero es limitada y no se puede utilizar en todas las situaciones.

Diferencias y limitaciones:

- No tiene sus propios enlaces a this o super y no se debe usar como métodos.
- No tiene argumentos o palabras clave new.target.
- No apta para los métodos call, apply y bind, que generalmente se basan en establecer un ámbito o alcance
- No se puede utilizar como constructor.
- No se puede utilizar yield dentro de su cuerpo.

<div id='sintaxisFuncionesFlecha'>

#### Sintaxis Funciones Flecha

```text
param => expression
```

<div id='ejemploFuncionesFlecha'>

#### Ejemplo (Funciones Flecha)

```javascript
const calcular_ventas = (unidades_a, unidades_b, unidades_c) => {
   return unidades_a*79 + unidades_b * 129 + unidades_c * 699;
}
console.log( calcular_ventas(10,50,30))
/*
Salida
28210
*/
```

<div id='ejemploDeLoAprendido'>

# Ejemplo de lo aprendido

```javascript
// Funcion de Flecha
const tipo_caracter = (operacion = "") => {
    let caracter = "";
    // switch
    switch(operacion) {
        case "suma":
            caracter = "+";
            break;
        case "resta":
            caracter = "-";
            break;
        case "miltiplicacion":
            caracter = "*";
            break;
        case "division":
            caracter = "/";
            break;
    }
    return caracter;
}
// function
function f_triangulo( largo_triangulo = 0, operacion = "" ) {
    // declaracion de variables
    const caracter = tipo_caracter(operacion);
    let resta_largo_triangulo = 0;
    let triangulo = "\n";

    // do...while
    do {
        let linea_triangulo = "";
        
        let final_espacios = (largo_triangulo-resta_largo_triangulo)/2;
        // while
        while( final_espacios > 0 ) {
            linea_triangulo += (final_espacios === 1 && resta_largo_triangulo === 0) ? ":)" : " ";
            final_espacios--
        }
        
        // for
        for( let i = 0; i < resta_largo_triangulo; i++ ) {
            linea_triangulo += caracter
        }
        triangulo += linea_triangulo+"\n";
        resta_largo_triangulo += 2;
    } while(resta_largo_triangulo <= largo_triangulo)
    console.log(triangulo)
}

//llamada a la funcion
f_triangulo(10, "suma")
f_triangulo(10, "resta")
f_triangulo(10, "miltiplicacion")
f_triangulo(10, "division")
```
