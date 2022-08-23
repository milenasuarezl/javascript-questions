# Javascript questions 

## Passing by value Passing by references

## Scope var, let and const

## Object reference 

let x = { foo: 'bar' }
let y = x
x.foo ='baz'
// y.foo?
"baz"

## Strict equality operator 
function greeting(name) {
  const person = { name: 'Ana', country: 'Bogota'};
  if (person === name) {
      console.warn('Hey Bogota')
  } else {
      console.warn('Hey Ana')
  }
}

greeting({ name: 'Ana', country: 'Bogota'})

// Hey Ana 

## Closure 

## Hoisting

## Binding scoping 

.bind() .apply() .call()

## Prottype

var a = 'a'
let b = 'b'

function (c) {
    let d = 'd'
    for(let i = 0; i < 10; i++) {
        const e = 'e'
        var f = 'f'
    }
}

const x = {
  baz: 'abz',
  foo() {
     function x() {
        console.log(this.baz)
     }

     const y = () => {
         console.log(this.baz)
     }

     x()
     y()
   }
}

console.log(x)
var x = 'foo'

# Promises

function getUserByName(name) {
    const user = { id: 1, name }
    return Promise.resolve(user)
}

function getPostsByUserId(userId) {
    const posts = [{ userId, title: 'title'}]
    return Promise.resolve(posts)
}



ANGULAR QUESTIONS
* ¿Cómo funciona el ciclo de vida en Angular?
* ¿Has usado rxjs? ¿En qué escenarios?
    R: normalmente rxjs se usa para hacer peticiones asincronas, como por ejemplo, obtener la data desde un servicio y transformarla, para que sea de facil manipulacion por la aplicacion
* ¿Qué técnicas de optimización implementas normalmente?
    R: lazy loading, optimizar assets
* ¿Cómo puedo compartir data de un componente padre a un componente hijo y viceversa? y compartir data entre paginas
    R: por ejemplo, usando Input. Y como compartir data desde un hijo hacia el padre? por ejemplo, usando Outputs. o compartir data entre paginas? por ejemplo, usando un servicio 
* ¿Cómo funcionan los observables?
* ¿Qué es el data binding? 
    R: Data binding in AngularJS is the synchronization between the model and the view. When data in the model changes, the view reflects the change, and when data in the view changes, the model is updated as well.

REACT QUESTIONS
* ciclo de vida
* hooks
* use effect
* props vs state
* context
* virtual DOM
* styled components

Redux
* What are reducers in redux?
The reducer is a pure function that takes the previous state and an action, and returns the next state.
* What is Redux Thunk?
Redux Thunk middleware allows you to write action creators that return a function instead of an action. The thunk can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met. The inner function receives the store methods dispatch and getState() as parameters.
*What is the difference between React context and React redux?


JS QUESTIONS
* ¿Puedes crear un div en el html y editar su contenido desde JS?
* Escribiendo un array de objetos, pueden ser 3 objetos con nombre, raza y edad.
* Podrías crear una función que solo imprima el nombre de los perros con edades pares.
* 
    var a = { name: 'John' , lastName: 'Doe'};
    var b = a;
    a.name = 'Alex';
    //b ?

    R: {name: 'Alex', lastname: 'Doe'}
* if(variable)
* tipos de datos primitivos


Funciones:
* ¿Qué tipos de funciones conoces?
* ¿Puedes escribir una función que pueda ser llamada de la siguiente manera: f(a)(b)?
* ¿Qué es IIFE?

Scope:
    * ¿Cuál es la diferencia entre arrow function y funciones tradicionales?
    * ¿Cuál es la diferencia entre context y scope?
    * ¿A qué hace referencia el "this"?
        R: the value of this is determined by how a function is called (runtime binding)
    * ¿Puedes decirme la diferencia entre call, apply y bind?
        R: ES5 introduced the bind() method to set the value of a function's this regardless of how it's called.


Closure
* ¿Qué es un closure? ¿Puedes hacer un ejemplo? ¿Para qué sirve? ¿En qué caso lo usarias?
* 
    function makeFunc() {
        console.log(name);
        function displayName() {
            var name = 'Juan';
        }
        return displayName();
    }
    makeFunc();
    
Hoisting
* 
    console.log(name);
    let name = 'Jey'  

 R: name is not defined, con var sale undefined  

Events:
* Tengo un div con un hijo, cada uno de los elementos tiene un evento onClick con un alert diferente. Si hago click al hijo. ¿Qué pasaría? 
    * Y en el caso contrario, haciendo click al padre?
    * ¿Cómo detengo ese comportamiento?

Promesas:
* ¿Cómo funcionan las promesas? ¿Puedes escribir una?
* ¿Cuál es la diferencia entre promise y callback?
    R: Callbacks. La llamada asíncrona recibe como parámetro una función. ... La llamada asíncrona retorna como resultado "provisional" una Promise. Este es un objeto que contendrá en el futuro el resultado.
* ¿Cómo funciona el async/await?
* ¿Cuál es la diferencia entre observables y promesas?
    R: Las promesas y los observables se ejecutan de forma asíncrona, la principal diferencia entre ambos es que mientras las promesas devuelven un único resultado, los Observables nos permiten definir una secuencia a partir de todos los métodos que nos ofrecen.
* ¿Cuales son los estados de una promesa?
	R:  pending: initial state, neither fulfilled nor rejected.
	    fulfilled: meaning that the operation was completed successfully.
        rejected: meaning that the operation failed.

Prototypes:
* What is a prototype? R: A prototype is an object from which other objects inherit properties
* Can any object be a prototype? R: Yes.
* Which objects have prototypes? R: Every object has a prototype by default. Since prototypes are themselves objects, every prototype has a prototype too. (There is only one exception, the default object prototype at the top of every prototype chain. More on prototype chains later)
* 
    var obj = function () {
        this.a = 'a';
    }
    obj.prototype.a = 'x';
    obj.prototype.b = 'y';
  
    var objInstance = new obj();
    console.log(objInstance.a)

OOP:
* ¿Puedes una clase con un método? Y crear una instancia de la clase que acceda al método.
* Puedes implementar un método estático y llamarlo.
* Asignar una propiedad al momento de la instanciación 
* Tienes clase perro, y tienes 100 perros instanciados, y quieres crear un método nuevo que tengan todos los perros, ¿cómo lo harías?

ES6/7
* 
    function myFunction(param1, param2, ...others) { return null; }

Patrones de diseño
* ¿Qué patrones de diseño manejas?
* Patron módulo (Tiene que saber de IIFE), modulo reveleado, singleton, patrón observer

Unit test:
* ¿Cuál es la diferencia entre unit test, test integration, end to end?
* funcionalidad que te haya tocado y que probaste
* ¿qué es un mock? ¿para que se usa?

Git:
rebase cherry pick, problemas al hacer merge
