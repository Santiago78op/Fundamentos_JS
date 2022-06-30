# Fundamentos

## Variable
Es un lugar en la memoria de nuestra computadora para almecenar datos.

## Ambito de existencias o Scope
Scope global y uno funcional, es decir las variables que existen dentro de una funcion van a estar disponibles a lo largo de esta funcion.

El ambito de bloque no existia en Js, la variable era colocada en el ambito global en js a esto se le llamaba elavación.

Pero esto cambio con ECMAScript6 desde el 2015

El objeto **window** mapea todo el ambito global del lenguaje JS.

Un bloque esta definodo por llabes {}.

- //comentario una linea
- /* Comentario varias lineas */

Es una mala practica utilizar **var**

### JavaScript
```js
    // ambito global
    var hola = "Hola Mundo"
    // ambito de bloque
    let hello = "Hello Word"
    console.log(hola)

    //comentario una linea
    /*
    Comentario varias lineas
    */
    console.log("*********VAR************")
    var musica = "rocl"
    console.log("variable musica antes del blque", musica)
    
    {
        var musica = "Pop"
        console.log("variable musica antes del bloque", musica)

    }
    console.log("variable musica despues del bloque", musica)
    
    console.log("*********LET************")
    let musica2 = "rocl"
    console.log("variable musica antes del blque", musica2)
    
    {
        let musica2 = "Pop"
        console.log("variable musica antes del bloque", musica2)

    }
    console.log("variable musica despues del bloque", musica2)
```

### Valores Primitivos
Son aquellos que accedemos directamente

### Valores Compuestos
Son aquellos que accedemos por medio de instacias


## const -> constante
Los objetos declarados con const que sea datos tipo compuesto si se pueden modificar ya no accedes al valor directamente sino a una instancia de este.

## String
- Objeto: Coleccion de informacion.
- Propiedades: Atributos de un objeto el cual brinda informacion sobre el mismo.
- Metodos: Son acciones que el objeto hace. Todos los metodos terminan con parentesis.
  
```js
    // const crear variables constantes
    const PI = 3.1416
    console.log(PI)

    // objeto

    let objeto = {
        nombre: "santi",
        edad: 35
    }

    let colores = ['rojo','azul','amarillo']

    console.log(objeto)
    console.log(colores)
    
    objeto.correo = "santi@gmail.com"
    colores.push("anaranjado")
```

# Cadenas de Texto

#### trim, split 
- Quita espacios en blanco que aparecen al inicio y final.
- Convertir string to array.

```js
    // Cadenas de Texto aka String

    let nombre = "Jon"
    let apellido = ''
    let lorem = 'hola como estas amet'

    // new permite crear un objeto nuevo
    let saludo = new String("Hola Mundo")

    console.log(nombre,apellido)
    // Con propiedades
    console.log(nombre.length,apellido.length,saludo.length)

    // Metodos
    console.log(nombre.toUpperCase(),apellido.toUpperCase(),saludo.toLocaleLowerCase(),lorem.includes("amet"), lorem.trim(), lorem.split(" "))    
```

## Concatener
Es unir variables ya sea del mismo o diferente tipo.

## Inerpolacion de variables
Metener en una cadena de texto, valores de una variable. Esta se hace con la comilla invertida `.

# DOM
Es el api que tiene javaScript en los navegadores para interactuar con html.

```js
    let nombre = "Jon"
    let apellido = 'lopez'

    // Concatenacion
    let saludo = "Hola mi nombre es " + nombre + " " + apellido + "."

    // Inerpolacion de variables
    let saludo2 = `Hola mi nombre es ${nombre} ${apellido}.`
    
    let ul = "<ul><li>Primavera</li><li>Verano</li><li>Otoño<li><li>Invierno</li></ul>"

    let ul2 = `
    <ul>
        <li>Primavera</li>
        <li>Verano</li>
        <li>Otoño</li>
        <li>Invierno</li>
    </ul>
    ` 
```

## Metodos para numeros

```js
    let a = 2
    let b = new Number(1)
    let c = 7.19
    let d = "5.6"

    // De que tipo de dato es una variable
    console.log(typeof c, typeof d)

    console.log(a,b)
    // cuantos numeros decimales tiene tu valor numerico
    console.log(c.toFixed(1))
    console.log(parseInt(c))
    console.log(parseFloat(c))
    // lo suma
    console.log(a+b)
    // procede a concatenar las variables
    console.log(c+d)
```

##  Verdadero o Falso

### Truthy

En JavaScript, un valor verdadero es un valor que se considera  true/verdadero cuando es evaluado en un contexto Booleano,en su defecto son Truthy. Todos los valores son verdaderos a menos que se definan como falso (es decir, excepto false, 0, "", null, undefined, y NaN).

Ejemplos de valores verdaderos en JavaScript (los cuales se traducirán a verdaderos y por lo tanto ejecutarán el bloque condicional if):

```js
if (true)
if ({})
if ([])
if (42)
if ("foo")
if (new Date())
if (-42)
if (3.14)
if (-3.14)
if (Infinity)
if (-Infinity)
```

### Falsy

Un valor falso (a veces escrito falsey) es un valor que se considera falso cuando se encuentra en un contexto booleano.

JavaScript utiliza la conversión de tipos para coaccionar cualquier valor a un booleano en contextos que lo requieren, como los condicionales y los bucles.

```js
if (false)
if (null)
if (undefined)
if (0)
if (-0)
if (0n)
if (NaN)
if ("")
```


```js
    let verdadero = true
    let falso = false
    let v = Boolean(true)
    let f = Boolean(false)

    console.log(verdadero,v,f,falso)
    console.log(typeof verdadero,typeof falso)

    //Variables que tienden a ser verdaderos o falsos
    console.log(Boolean(0))//false por que no se ha inicializado el valor.
    console.log(Boolean(-7))//verdadero por que ya se inicializo el valor.
    console.log(Boolean(""))//false por que la cadena no contiene nada.
    console.log(Boolena("."))//verdadero por que ya se fue incilizada la cadena.
```

## Null and Undefined
Los van a representar un valor ausente.

- Undefined: es una variable que no a sido inicializada y que no cuenta con valor.
- Null: es un valor especial que significa que la variable esta vacia intencionalmente asignado por programador como sin valor.

```js
    let indefinida

    let nulo = null
    console.log(nulo)
```

## NaN Not a Number
Se esta haciendo operaciones aritmeticas entre variables que no son de tipo numero.

# Compuestos

## Ordenamiento de Codigo

1. Importación de Modulos.
2. Declaracion de Variables.
3. Declaracion de Funciones.
4. Ejecucion de codigo.

## Funciones
Una función es un bloque de código, autocontenido, que se puede definir una vez y ejecutar en cualquier momento. Opcionalemente, una función puede aceptar parámetros y devolver un valor.

Las funciones en JavaScript son objetos, un tipo especial de objetos.

Se dice que estas en javaScript son ciudadanos de primera clase porque pueden asignarse a un valor, y pueden pasarse como argumentos y usarse como un valor de retorno.

Se va a definir una solo vez y se podra reutilizar tantetes veces como sea necesario, ademas puede o no retornar valor. Estas son un tipo de objeto especail: se dice que estas en javaScript son ciudadanos de primera clase.

Las arrow functions son un caso especial de estas.

- Funciones Declaradas
- Funciones Expresadas -> es una buena practica

```js
// Fuciones Declarada
function estoEsUnaFuncion(){
    console.log("Uno")
    console.log("Dos")
    console.log("Tres")
}

function unaFuncionQueDevuelveValor(){
    return "La funcion fue ejecutada y retorna valor"
}

// Invocación de función
estoEsUnaFuncion()
// los parentesis indican que una accion se va a ejecutar.
// Se ejecutara 4 veces, esta funcion no recibe parametro ni devuleve valores.
estoEsUnaFuncion()
estoEsUnaFuncion()
estoEsUnaFuncion()
estoEsUnaFuncion()

// Retorna valor
let valor = unaFuncionQueDevuelveValor()
console.log(valor)

//Funcion con parametros
function saludar(nombre,edad){
    console.log(`Hola mi nombre es ${nombre} y tengo ${edad} años.`,)
}

saludar("santi",8)
// se hace uso de undifine
saludar()
// pero se pueden modificar 
function saludar(nombre = "desconocido",edad = 0){
    console.log(`Hola mi nombre es ${nombre} y tengo ${edad} años.`,)
}

// lo que hace es elevar el nivel de la funcion para que la puedes utilizar de esta manera

funcionDeclarada()

// Funciones Declaras vs Funciones Expresadas
function funcionDeclarada(){
    console.log("Esto es una funcion declarada puede invocarse en cualquier parte de nuestro codigo incluso antes de que la funcion sea declarada")
}

funcionDeclarada()

// no puedes acceder a esta antes de su inicializacion. begore initialization.

funcionExpresada()

// Funciones Expresadas
// No es necesario el nombre ya que se lo da la variable.
// funcion anonima.
const funcionExpresada = function (){
    console.log("Esto es una funcion expresada que se le ha asignado como valor a una variable, si invocamos esta funcion antes de su definicion JS nos dira...")
}

funcionExpresada()
```

## Datos Compuestos Arreglos
Pueden ser declarados con let o const, en estos se accede a la referencia del valor.

Son mas de 20 metodos.

```js

const a = []
const b = [1,true,"hola",["a","b","c"]] 
console.log(a)
console.log(b.length)
console.log(b[2])
console.log(b[3][2])


// nuevo metodo apartir del 2015
const c = Array.of["x","y","z",9,8,7]
console.log(c)

const d = Array(5).fill(false)

// Formas antiguas de declarar arreglos

const e = new Array()

const f = new Array(1,2,3,true,false)

// Otros arreglos
const colores = ["rojo","verde","azul"]
console.log(colores)

// agregar nuevo volor en el la ultima posicion
colores.push("negro")
console.log(colores)

// Elimina un volor en el la ultima posicion
colores.pop()
console.log(colores)

//Ejecutar una funcion por cada elemento que tenga el arreglo

// el valor con el primer parametro, la posicion que ocupa en el arreglo padre.
colores.forEach(function(elemento, index){
    console.log(`<li id="${index}">${elemento}</li>`)
})
```

## Objetos 
frase en javascript todo es un objeto. Un objeto es una coleccion de llave valores.

Los objetos dentro de un objeto a las variables se les llamara atributos/propiedades y a las funciones se les llama metodos.

```js
let a = new String("Hola")

const b = {}

console.log(b)

const c = new Object()
console.log(c)

const santy = {
    nombre: "santiago",
    apellido: "Barrera",
    edad: 23,
    pasatiempos: ["Correr", "Hacer ejercicio"],
    soltero: true,
    contacto: { 
        gmail:"santiago@gmail.com",
        movil: 3568749
    },
    saludar: function(){
        console.log("Hola :)")
    },
    decirMiNombre: function(){
        console.log(`Hola me llamo ${this.nombre} ${this.apellido}.`)
        this.saludar()
    }
}

santy.saludar()
santy.decirMiNombre()

console.log(Object.keys(santy))
console.log(Object.values(santy))
console.log(santy.hasOwnProperty("nombre"))
console.log(santy.hasOwnProperty("apellido"))
console.log(santy.hasOwnProperty("carro"))
```