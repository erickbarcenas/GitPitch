![Logo](http://arquitectura.unam.mx/uploads/8/1/1/0/8110907/_2634437.png?131)
## Universidad Nacional Autónoma de México
### Facultad de Ingeniería
#### 

---
### Temario

- @color[gray](Importancia del software en la mecatrónica) |
- Metodología de la programación orientada a objetos |
- Desarrollo de sistemas de cómputo orientados a objetos |
- Concepto, uso y aplicaciones de las estructuras de datos compuestas |
- Interfaces gráficas de usuario |
--- 


### 2. Metodología de la programación orientada a objetos

<br>

#### Objetivo:
El alumno descubrirá los fundamentos del paradigma de programación orientado a objetos.
---

### Contenido

- Clases y objetos. Constructores, atributos y métodos |
- Encapsulación, herencia y polimorfismo |
- Sobrecarga de funciones |
- Sobrecarga de operadores |
- Manejo de errores y de excepciones |
- Arreglos y colecciones |
- Implementación de interfaces |
- Manejadores de eventos |
- Construcción de bibliotecas y reutilización de código |
- Almacenamiento, actualización y eliminación de información en base a estructuras |
- Manejo de archivos (escritura, lectura, acceso secuencial, acceso aleatorio)|

---
##### [C#]

- [Un paseo por C#](https://docs.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/)
- Tipos y variables
- [Expresiones](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/statement-keywords)

---
##### Say Hello

```
using System;

class Hello
{
    static void Main()
    {
        Console.WriteLine("Hello, World");
		Console.Read();
    }
}
```

---
##### Ejemplos Tipos y variables [int]


```
class Program
{ 
   static void Main(string[] args) 
   {
      int num=30;
      Console.Write(num);
	  Console.Read();
   }
}
```

---
##### Ejemplos Tipos y variables [double]


```
 class Program
 { 
  static void Main(string[] args) 
  {
   double num=30.33;
   Console.Write(num); 
   Console.Read();
  }
```
---
##### Ejemplos Tipos y variables [Boolean]


```
class Program
{ 
   static void Main(string[] args) 
   {
      Boolean status=true;
      Console.Write(status);
	  Console.Read();
   }
}

```

---

##### Ejemplos Tipos y variables [String]


```
class program
{
   static void Main(string[] args)
   {
      String message="Hello";
      Console.Write(message);
	  Console.Read();
   }
}

```
---

- [Instrucciones](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/statement-keywords)

---

@fa[github fa-4x fa-spin]


-[Git / GitHub](https://www.github.com)
-[Hello World](https://guides.github.com/activities/hello-world/)
-[Cheat Sheet](https://services.github.com/on-demand/downloads/es_ES/github-git-cheat-sheet.pdf)

---
** Say hello 2 **

```
/* using keyword is used to include the System 
   namespace in the program */
using System; // 

/* A namespace is a collection of classes*/
namespace HelloWorldApplication {

   /* Classes generally contain multiple methods. 
   Methods define the behavior of the class. 
   However, the HelloWorld class has only one method Main.*/
   class HelloWorld { // class declaration. 
   
      /*Main method, which is the entry point 
	  for all C# programs*/
      static void Main(string[] args) {
	  
	     /* WriteLine is a method of the Console class 
		 defined in the System namespace. 
		 This statement causes the message 
		 "Hello, World!" to be displayed on the screen.*/
         Console.WriteLine("Hello World");

		 /*This makes the program wait for a key press 
		 and it prevents the screen from running and 
		 closing quickly*/
         Console.ReadKey(); 
      }
   }
}
```
---

### Contenido

- Clases y objetos. Constructores, atributos y métodos

---
### Class

Clase en C#

Cuando se define una clase (**class**), define un *modelo* para un tipo de datos. Esto en realidad no define ningún dato, pero define lo que significa el nombre de clase. Es decir, en qué consiste el objeto de la clase y qué operaciones se pueden realizar en ese objeto. Los objetos son instancias de una clase. Los métodos y variables que constituyen una clase se llaman miembros de la clase.

---
### Object

Objeto en C#

Un objeto es una entidad. Esto quiere decir que puede "verse" y "sentirse".
---
### Method

Método en C#

Un método define el comportamiento de los objetos de una clase.

---
*Hands on classes*

Defina las clases para los siguientes elementos

* Perro
* Coche

---
### Constructor

Un constructor en C#

Es una miembro especial de la clase que es ejecutada cuando se crea un nuevo objeto de la clase.
Un Constructor tiene exactamente el mismo nombre que la clase que la define y no tiene ningún tipo de retorno.
Un constructor parametrizado es aquel que es utilizado para asignar valores iniciales a un objeto al tiempo de su creación.

---
*Hands on classes*

Defina los constructores para las clases previamente creadas

* Perro
* Coche

---
### *Practica 1*

1. *Objetivos de aprendizaje* 
 
I. Objetivos generales:  Entender la diferencia entre clase y objeto. 
II. Objetivos específicos:
 
* Aprender a diseñar clases. 
* Entender el funcionamiento de los constructores. 
* Identificar los atributos y los métodos. 
* Aprender a crear objetos. 

---
#### *Encapsulación, herencia y polimorfismo*

Encapsulación

La encapsulación se define 'como el proceso de adjuntar uno o más elementos dentro de un paquete físico o lógico'. La encapsulación, en la metodología de programación orientada a objetos, impide el acceso a los detalles de implementación.

---

##### *Encapsulación*

La encapsulación es implementada utilizando *access specifiers*. 
Un *access specifier* define el alcance y la visibilidad de un miembro de la clase. C# soporta los siguiente *access specifier*

* Public
* Private
* Protected
* Internal
* Protected internal
---
##### *Encapsulación*

***Public and Private***

*Public* Es el modificador menos restrictivo. No existen restricciones para el acceso a los miembros o tipos que se hayan definido mediante public.

*Private* Los miembros privados sólo son accesibles dentro de la clase en la que se definen. Es por tanto el modificador más restrictivo.
---
##### *Encapsulación*

**Internal**

El modificador internal indica que aquellos miembros o tipos que se hayan definido con este modificador de acceso sólo serán accesibles desde los archivos del mismo ensamblado.

---
##### *Encapsulación*

**Protected and Protected Internal**

El modificador protected indica que sólo la clase en la que se ha utilizado el modificador y sus clases derivadas tendrán acceso al miembro o tipo definido como protected.
El modificador protected internal permite a la clase esconder sus variables y sus funciones de otra clase, objetos y funciones, excepto a la clase hijo de la misma aplicación.
---
##### *Herencia*

La herencia nos permite definir a una clase en términos de otra clase, lo que hace fácil crear y mantener una aplicación. Esto también provee la oportunidad de reusar funcionalidad de código y acelara el tiempo de implementación.
* Se utiliza cuando existen clases que comparten muchas de sus características
* Se extiende su funcionalidad a clases más genéricas
* Se introducen conceptos como *superclase* y *subclase*
---

```
using System;

namespace AplicacionHerencia {
   class ProbadorDeRectangulo {
      static void Main(string[] args) {
         Rectangulo Rect = new Rectangulo();

         Rect.setAncho(5);
         Rect.setAlto(7);

         // Print the area of the object.
         Console.WriteLine("Área Total: {0}",  Rect.getArea());
         Console.ReadKey();
      }
   }
   
   class Forma {
      protected int ancho;
      protected int alto;
	  
      public void setAncho(int w) {
         ancho = w;
      }
      public void setAlto(int h) {
         alto = h;
      }
   }

   // Clase derivada
   class Rectangulo: Forma {
      public int getArea() { 
         return (ancho * alto); 
      }
   }
}
``` 
---

### *Examen 1 08/16/2018* 

Desarrollar un programa en la consola de C# para realizar la suma y la divición de dos números, a partir de valores proporcionados por el usuario y mostrando los resultados correspondientes en pantalla
* El programa debe de contener el uso de clases, objetos, métodos y constructores.
* Al terminar el examen subir el programa a un repositorio personal y los resultados de las pruebas en un archivo txt a un repositorio personal llamado *Examenes*
* Enviar el link al repositorio mediante el classroom de google.
* La calificación del examen se aplicará a la práctica 0.
---

##### [Polimorfismo](http://www.itnuevolaredo.edu.mx/takeyas/Apuntes/POO/Apuntes/04.-Polimorfismo.pdf)

Es la habilidad que poseen los objetos para reaccionar de modo diferente ante los mismos mensajes.

El polimorfismo se refiere a la posibilidad de definir múltiples clases con funcionalidad diferente, pero con métodos o propiedades denominados de forma idéntica, que pueden utilizarse de manera intercambiable mediante código cliente en tiempo de ejecución.

En C# el polimorfismo está íntimamente relacionado con la sobrecarga y métodos virtuales.

---

##### Ejemplo 1

``` 
using System;

namespace PolymorphismApplication {
   class Printdata {
      void print(int i) {
         Console.WriteLine("Printing int: {0}", i );
      }
      void print(double f) {
         Console.WriteLine("Printing float: {0}" , f);
      }
      void print(string s) {
         Console.WriteLine("Printing string: {0}", s);
      }
      static void Main(string[] args) {
         Printdata p = new Printdata();
         
         // Call print to print integer
         p.print(5);
         
         // Call print to print float
         p.print(500.263);
         
         // Call print to print string
         p.print("Hello C++");
         Console.ReadKey();
      }
   }
}
``` 

---
##### Ejemplo 2

``` 
using System;

namespace PolymorphismApplication {
   abstract class Shape {
      public abstract int area();
   }
   
   class Rectangle:  Shape {
      private int length;
      private int width;
      
      public Rectangle( int a = 0, int b = 0) {
         length = a;
         width = b;
      }
      public override int area () { 
         Console.WriteLine("Rectangle class area :");
         return (width * length); 
      }
   }
   class RectangleTester {
      static void Main(string[] args) {
         Rectangle r = new Rectangle(10, 7);
         double a = r.area();
         Console.WriteLine("Area: {0}",a);
         Console.ReadKey();
      }
   }
}
``` 
---
#### Métodos, sobrecarga y sobreescritura

Creación de métodos, sobrecarga y sobreescritura.

Son procedimientos o funciones definidos dentro de una CLASE. Los métodos pueden manejar los campos de la clase incluso si son privados.

La sobrecarga es la creación dentro de la clase, de un grupo de métodos que tienen el mismo nombre pero con un número de parámetros distinto y/o bien distintos tipos de datos.
---

**Ejemplo 1**

```
public void visualización () {
  MessageBox.Show("Sr. "+Apellido+" "+Nombre+" nacido el "+FechaNac); 
}
 
public void visualización (string idioma) {
  switch (idioma) {
    case "es":  MessageBox.Show("Sr. "+Apellido+" "+Nombre+" nacido el "+FechaNac); break;
    case "en":  MessageBox.Show("Mr. "+Apellido+" "+Nombre+" was born "+FechaNac); break;
  }
}
```
---

Sabemos que las clases derivadas heredan las propiedades y métodos de su clase base. Se pueden usar sin ninguna modificación, pero sí el método no está adaptado a la nueva clase podemos sobrescribirlo. Para ello utilizamos la palabra reservada override. También es obligatorio que permitir la sobrescritura de mediante el de la palabra reservada virtual. Esto se utiliza para asegurar el polimorfismo entre las clases.

---
Ejemplo 2
```
public override void visualización () {
  MessageBox.Show("Sr. "+Apellido+" "+Nombre+" nacido el "+FechaNac+" cobra "+Salario+".-€uros/mes."); 
}
 
public sealead override void visualización () {
  base.visualizacion();
  MessageBox.Show("y cobra "+Salario+".-MXP/mes."); 
```

---
Ejemplo de método abstracto

```
  public abstract string EstadoCivil();
  //de este método no hay implementación sólo definición.
  // la clase también estará marcada como abstracta.
```

---

Métodos de extensión

Los métodos de extensión permiten añadir funcionalidades a una clase ya definida sin tener que modificar el código de esta clase. Se deben respetar las siguientes reglas:

* Pueden ser de tipo procedimientos o función. NUNCA propiedad.
* El primer parámetro irá precedido de la palabra this. La palabra clave this hace referencia a la instancia actual de la clase ,pero también se utiliza como modificador del primer parámetro de un método de extensión.
* El tipo del primer parámetro del método determina el tipo extendido por este método.
* En el momento de la ejecución, éste primer parámetro representa la instancia de la clase sobre la cual se llama el método.
* Se deben definir una clase static.
* Ellos mismos deben ser static.

---

```
static class ExtesionPersona {
    public static void presentacion(this Persona p) {
        Console.WriteLine("Apellido: {0}", p.apellido);
        Console.WriteLine("Nombre: {0}",p.nombre);
        Console.writeLine("Fecha de nacimiento: {0}", p.fecha_naci);
    }
}

```
---

Los métodos de extensión también también se pueden definir para los tipos básicos del Framework, como por ejemplo la clase string. El siguiente código añade a la clase string un método que permite convertir el primer carácter de una cadena en mayúsculas.

```
public static class ExtensionString
{
    public static string PrimeroMayusculas(this String s)
    {
        if ((s == null) || (s.Length == 0))
        {
            return s;
        }
        else if (s.Length == 1)
        {
 
            return s.ToUpper();
        }
        else
        {
            return s.Substring(0, 1).ToUpper() + s.Substring(1, s.Length - 1);
        }
    }
}
```
---
```
class Program
{
    static void Main(string[] args)
	{
	    Console.WriteLine(5.ElevadoALa(3));
		Console.WriteLine(7.ElevadoALa(2));
		15.Doble();
		Console.Read();
	}
	
	public static class IntegerExtensionsMethods
	{
	    public static double ElevadoALa(this int valor, int exponente)
		{
		    return Math.Pow(valor, exponente);
		}
		
		public static double Doble(this int valor)
		{
		    return valor *2;
		}
	}
}
```
---
### *Examen 2 08/28/2018* 

##### Desarrollar un programa en la consola de C# para obtener el área de un triangulo, un cuadrado y un circulo, a partir de valores proporcionados por el usuario y mostrando los resultados correspondientes en pantalla
###### El programa debe de contener el uso de clases, objetos, métodos, constructores, herencia y polimorfismo.
###### Al terminar el examen subir el programa a un repositorio personal y los resultados de las pruebas en un archivo txt a un repositorio personal llamado *Examenes*
###### Enviar el link al repositorio mediante el classroom de google.

---
##### [Sobrecarga de Operadores](https://docs.microsoft.com/es-es/dotnet/csharp/programming-guide/statements-expressions-operators/overloadable-operators)

```
public class Persona
{
    public Persona(double salario)
	{
	    Salario = salario;
	}
	
	public static double operator+(Persona x, Persona y)
	{
	    return x.Salario + y.Salario;
	}
	
	public double Salario {get;set;}
}

public class Program
{
    public static void Maid(string[] arg)
	{
	    Persona juan = new Persona(1000.0)
		Persona ana = new Persona(500.0)
		
		double salarioTotal = juan + ana;
		
		Console.WriteLine(salarioTotal);
		Console.Read();
	}
}

```
---

[Otros ejemplos](https://www.tutorialesprogramacionya.com/csharpya/detalleconcepto.php?codigo=197&inicio=60)

---
#### [Manejo de errores y de excepciones](https://www.tutorialspoint.com/csharp/csharp_exception_handling.htm)

An exception is a problem that arises during the execution of a program. A C# exception is a response to an exceptional circumstance that arises while a program is running, such as an attempt to divide by zero.

Exceptions provide a way to transfer control from one part of a program to another. C# exception handling is built upon four keywords: **try**, **catch**, **finally**, and **throw**.

---
#### Manejo de errores y de excepciones

**try** − A try block identifies a block of code for which particular exceptions is activated. It is followed by one or more catch blocks.

**catch** − A program catches an exception with an exception handler at the place in a program where you want to handle the problem. The catch keyword indicates the catching of an exception.
---
#### Manejo de errores y de excepciones

**finally** − The finally block is used to execute a given set of statements, whether an exception is thrown or not thrown. For example, if you open a file, it must be closed whether an exception is raised or not.

**throw** − A program throws an exception when a problem shows up. This is done using a throw keyword.

---
##### Syntax

```
try {
   // statements causing exception
} catch( ExceptionName e1 ) {
   // error handling code
} catch( ExceptionName e2 ) {
   // error handling code
} catch( ExceptionName eN ) {
   // error handling code
} finally {
   // statements to be executed
}
```

---

##### [Excepciones generadas por el compilador](https://docs.microsoft.com/es-es/dotnet/csharp/programming-guide/exceptions/compiler-generated-exceptions)

---
```
//DivideByZeroException Class
int number1 = 3000;
int number2 = 0;
try
{
    Console.WriteLine(number1 / number2);
}
catch (DivideByZeroException)
{
    Console.WriteLine("Division of {0} by zero.", number1);
}
```
---

```
//OverflowException Class 
int value = 780000000;
checked
{
    try
    {
        // Square the original value.
        int square = value * value;
        Console.WriteLine("{0} ^ 2 = {1}", value, square);
    }
    catch (OverflowException)
    {
        double square = Math.Pow(value, 2);
        Console.WriteLine("Exception: {0} > {1:E}.",
                          square, Int32.MaxValue);
    }
}
// The example displays the following output:
//       Exception: 6.084E+17 > 2.147484E+009.

```
---
```
//ArrayTypeMismatchException Class

string[] names = { "Dog", "Cat", "Fish" };
Object[] objs = (Object[])names;

try
{
    objs[2] = "Mouse";

    foreach (object animalName in objs)
    {
        System.Console.WriteLine(animalName);
    }
}
catch (System.ArrayTypeMismatchException)
{
    // Not reached; "Mouse" is of the correct type.
    System.Console.WriteLine("Exception Thrown.");
}

try
{
    Object obj = (Object)13;
    objs[2] = obj;
}
catch (System.ArrayTypeMismatchException)
{
    // Always reached, 13 is not a string.
    System.Console.WriteLine(
        "New element is not of the correct type.");
}

// Set objs to an array of objects instead of 
// an array of strings.
objs = new Object[3];
try
{
    objs[0] = (Object)"Turtle";
    objs[1] = (Object)12;
    objs[2] = (Object)2.341;

    foreach (object element in objs)
    {
        System.Console.WriteLine(element);
    }
}
catch (System.ArrayTypeMismatchException)
{
    // ArrayTypeMismatchException is not thrown this time.
    System.Console.WriteLine("Exception Thrown.");
}

```
---
```
// IndexOutOfRangeException Class 

List<Char> characters = new List<Char>();
characters.InsertRange(0, new Char[] { 'a', 'b', 'c', 'd', 'e', 'f' });
for (int ctr = 0; ctr <= characters.Count; ctr++)
    Console.Write("'{0}'    ", characters[ctr]);
	
```
---
##### [Excepciones generadas por el compilador](https://docs.microsoft.com/es-es/dotnet/csharp/programming-guide/exceptions/compiler-generated-exceptions)

###### [throw](https://docs.microsoft.com/es-mx/dotnet/csharp/language-reference/keywords/throw)

```
    class Program
    {
        static void Main(string[] args)
        {

            GeneradorDeNumeros Gnum = new GeneradorDeNumeros();

            Console.WriteLine(Convert.ToString(Gnum.GetNumero(2)));
            Console.Read();
        }
    }
		
	class GeneradorDeNumeros
    {
        int[] numeros = { 2, 4, 6, 8, 10, 12, 14, 16, 18, 20 };

        public int GetNumero(int indice)
        {
            if (indice < 0 || indice >= numeros.Length)
            {
                throw new IndexOutOfRangeException();
            }
            return numeros[indice];
        }
    }
		
```
---
###### [Operador Condicional **?**](https://docs.microsoft.com/es-mx/dotnet/csharp/language-reference/operators/conditional-operator)

```
int input = Convert.ToInt32(Console.ReadLine());  
string classify;  

// if-else construction.  
if (input > 0)  
    classify = "positive";  
else  
    classify = "negative";  

// ?: conditional operator.  
classify = (input > 0) ? "positive" : "negative";
```
---

###### [throw](https://docs.microsoft.com/es-mx/dotnet/csharp/language-reference/keywords/throw)

```
private static void DisplayFirstNumber(string[] args)
{
   string arg = args.Length >= 1 ? args[0] : 
                              throw new ArgumentException("You must supply an argument");
   if (Int64.TryParse(arg, out var number))
      Console.WriteLine($"You entered {number:F0}");
   else
      Console.WriteLine($"{arg} is not a number.");                            
}
```
---
###### [throw](https://docs.microsoft.com/es-mx/dotnet/csharp/language-reference/keywords/throw)

```
public string Name
{
    get => name;
    set => name = value ?? 
        throw new ArgumentNullException("Name cannot be null", nameof(value));
}   
```
---
##### [Arreglos](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/arrays/)

* Almacena una colección de elementos determinada y secuencial
* Solo se pueden almacenar elementos de un mismo tipo
* Pueden ser de todos los tipos: int, string, object, etc.

Estructura de un arreglo con longitud 4

|Valores|45|2|25|545|
|---|---|---|---|---|
|Índice|0|1|2|3|

---
##### [Arreglos](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/arrays/)

###### Declaración de un arreglo

```
dataType[] nombreDelArreglo;
int[] calificaciones;
```

###### Inicialización de un arreglo
```
dataType[] nombreDelArreglo = new dataType[número de elementos];
int[] calificaciones = new int[5];
```
---
##### [Arreglos](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/arrays/)

###### Asignación de valores a un arreglo

```
nombreDelArreglo[índice] = valor;

calificaciones[0]= 90;
calificaciones[1]= 50;
```

###### Lectura de valores a un arreglo

```
nombreDelArreglo[índice];
calificaciones[1];
```
---
### *Examen 3 09/04/2018* 

###### Dado el programa en el siguiente [link](https://github.com/lusan12/ExamenesTP/tree/master/EXAM2) obtenga el área de un triangulo, un rectángulo y un circulo, a partir de valores proporcionados por el usuario y mostrando los resultados correspondientes en pantalla
###### El programa debe de utilizar la sobrecarga de operadores vista en clase.
###### Al terminar el examen subir el programa a un repositorio personal y los resultados de las pruebas en un archivo txt a un repositorio personal llamado *Examenes*
###### Enviar el link al repositorio mediante el classroom de google.
---
###### Ejemplos
```
/* The following code assigns the length of the numbers array, 
 * which is 5, to a variable called lengthOfNumbers
 */
int[] numbers = { 1, 2, 3, 4, 5 };
int lengthOfNumbers = numbers.Length;

// Single-Dimensional Arrays
string[] stringArray = new string[6];
int[] array1 = new int[] { 1, 3, 5, 7, 9 };
int[] array2 = { 1, 3, 5, 7, 9 };
string[] weekDays = { "Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat" };

/* It is possible to declare an array variable without initialization, 
 * but you must use the new operator when you assign an array to this variable
 */
int[] array3;
array3 = new int[] { 1, 3, 5, 7, 9 };
```
---
###### Ejemplos
```
/* Multidimensional Arrays
/

/* the following declaration creates a two-dimensional array of four rows and 
 * two columns   
 */
int[,] array = new int[4, 2];

// Array Initialization

// Two-dimensional array.
int[,] array2D = new int[,] { { 1, 2 }, { 3, 4 }, { 5, 6 }, { 7, 8 } };
// The same array with dimensions specified.
int[,] array2Da = new int[4, 2] { { 1, 2 }, { 3, 4 }, { 5, 6 }, { 7, 8 } };
// A similar array with string elements.
string[,] array2Db = new string[3, 2] { { "one", "two" }, { "three", "four" },
                            { "five", "six" } };
```
---
###### Ejemplos
```
// Three-dimensional array.
int[,,] array3D = new int[,,] { { { 1, 2, 3 }, { 4, 5, 6 } },
                     { { 7, 8, 9 }, { 10, 11, 12 } } };
// The same array with dimensions specified.
int[,,] array3Da = new int[2, 2, 3] { { { 1, 2, 3 }, { 4, 5, 6 } },
                           { { 7, 8, 9 }, { 10, 11, 12 } } };

// Accessing array elements.
System.Console.WriteLine(array2D[0, 0]);
System.Console.WriteLine(array2D[0, 1]);
System.Console.WriteLine(array2D[1, 0]);
System.Console.WriteLine(array2D[1, 1]);
System.Console.WriteLine(array2D[3, 0]);
System.Console.WriteLine(array2Db[1, 0]);
System.Console.WriteLine(array3Da[1, 0, 1]);
System.Console.WriteLine(array3D[1, 1, 2]);
```
---
###### Ejemplos
```
// Getting the total count of elements or the length of a given dimension.
var allLength = array3D.Length;
var total = 1;
for (int i = 0; i < array3D.Rank; i++)
{
    total *= array3D.GetLength(i);
}
System.Console.WriteLine("{0} equals {1}", allLength, total);
Console.Read();

//You also can initialize the array without specifying the rank.
int[,] array4 = { { 1, 2 }, { 3, 4 }, { 5, 6 }, { 7, 8 } };
```
---
###### Ejemplos
```
/* If you choose to declare an array variable without initialization, 
 * you must use the new operator to assign an array to the variable
 */
int[,] array5;
array5 = new int[,] { { 1, 2 }, { 3, 4 }, { 5, 6 }, { 7, 8 } };   // OK
//array5 = {{1,2}, {3,4}, {5,6}, {7,8}};   // Error

//The following example assigns a value to a particular array element.
array5[2, 1] = 25;

/* Similarly, the following example gets the value of a particular 
 * array element and assigns it to variable elementValue
 */
int elementValue = array5[2, 1];

/* The following code example initializes the array elements to default values */
int[,] array6 = new int[10, 10];
```
---
###### Ejemplos
```
/* Jagged Arrays - Arreglo de arreglos */
/* he following is a declaration of a single-dimensional array that has three 
 * elements, each of which is a single-dimensional array of integers
 */

int[][] jaggedArray = new int[3][];

/* Before you can use jaggedArray, its elements must be initialized. You can 
 * initialize the elements like this: Before you can use jaggedArray, its elements 
 * must be initialized. You can initialize the elements like this:
 */

jaggedArray[0] = new int[5];
jaggedArray[1] = new int[4];
jaggedArray[2] = new int[2];

// OR

jaggedArray[0] = new int[] { 1, 3, 5, 7, 9 };
jaggedArray[1] = new int[] { 0, 2, 4, 6 };
jaggedArray[2] = new int[] { 11, 22 };

// OR

int[][] jaggedArray2 = new int[][]
{
      new int[] {1,3,5,7,9},
      new int[] {0,2,4,6},
      new int[] {11,22}
};

//OR 

int[][] jaggedArray3 =
{
     new int[] {1,3,5,7,9},
     new int[] {0,2,4,6},
     new int[] {11,22}
};
```
---
###### Ejemplos
```
/* access individual array elements */

// Assign 77 to the second element ([1]) of the first array ([0]):
jaggedArray3[0][1] = 77;

// Assign 88 to the second element ([1]) of the third array ([2]):
jaggedArray3[2][1] = 88;

/* It is possible to mix jagged and multidimensional arrays. 
 * The following is a declaration and initialization of a single-dimensional 
 * jagged array that contains three two-dimensional array elements 
 * of different sizes.
 */

int[][,] jaggedArray4 = new int[3][,]
{
    new int[,] { {1,3}, {5,7} },
    new int[,] { {0,2}, {4,6}, {8,10} },
    new int[,] { {11,22}, {99,88}, {0,9} }
};

/* You can access individual elements as shown in this example,
 * which displays the value of the element [1,0] of the first array
 */
System.Console.Write("{0}", jaggedArray4[0][1, 0]);
```
---
###### Ejemplos
```
// Using foreach with Arrays //
/* For single-dimensional arrays, the foreach statement processes elements 
 * in increasing index order, starting with index 0 and ending with index 
 * Length - 1:
 */

int[] numbers1 = { 4, 5, 6, 1, 2, 3, -2, -1, 0 };
foreach (int i in numbers1)
{
    System.Console.Write("{0} ", i);
}
Console.Read();

/* For multi-dimensional arrays, elements are traversed such that the indices 
 * of the rightmost dimension are increased first, then the next left dimension, 
 * and so on to the left
 */
int[,] numbers2D = new int[3, 2] { { 9, 99 }, { 3, 33 }, { 5, 55 } };
// Or use the short form:
// int[,] numbers2D = { { 9, 99 }, { 3, 33 }, { 5, 55 } };

foreach (int i in numbers2D)
{
    System.Console.Write("{0} ", i);
}
// Output: 9 99 3 33 5 55
```
---
###### Ejemplos
```
// Passing arrays as arguments

int[] theArray = { 1, 3, 5, 7, 9 };
PrintArray(theArray);

int[,] theArray2 = { { 1, 2 }, { 2, 3 }, { 3, 4 } };
Print2DArray(theArray2);
}

static void PrintArray(int[] arr)
{
    // Method code.
}

static void Print2DArray(int[,] arr)
{
    // Method code.
}
```
---
#### Colecciones
https://msdn.microsoft.com/es-es/library/ybcx56wz(v=vs.120).aspx

En muchas aplicaciones se desea poder crear y administrar grupos de objetos relacionados. Existen dos formas de agrupar objetos: mediante la creación de matrices de objetos y mediante la creación de colecciones de objetos. 
 
Las colecciones proporcionan un método más flexible para trabajar con grupos de objetos. A diferencia de las matrices, el grupo de objetos con el que trabaja puede aumentar y reducirse dinámicamente a medida que cambian las necesidades de la aplicación.

---
##### [List](https://docs.microsoft.com/es-es/dotnet/api/system.collections.generic.list-1?redirectedfrom=MSDN&view=netframework-4.7.2)

Representa una lista de objetos fuertemente tipados a la que se puede obtener acceso por índice. Proporciona métodos para buscar, ordenar y manipular listas.

---
##### [Queue](https://docs.microsoft.com/es-es/dotnet/api/system.collections.generic.queue-1?redirectedfrom=MSDN&view=netframework-4.7.2)

Representa una colección de objetos de tipo primero en entrar, primero en salir.

---
##### [Stack](https://docs.microsoft.com/es-es/dotnet/api/system.collections.generic.stack-1?redirectedfrom=MSDN&view=netframework-4.7.2)

Representa una colección último en entrar, primero en salir (LIFO) de tamaño variable con instancias del mismo tipo especificado.

---
##### [Interfaces](https://docs.microsoft.com/es-mx/dotnet/csharp/programming-guide/interfaces/)

Una interfaz se define como un contrato sintáctico que deben seguir todas las clases que heredan la interfaz. La interfaz define la parte **qué** del contrato sintáctico y las clases derivadas definen la parte **cómo** del contrato sintáctico.
---
###### [Declarando Interfaces](https://www.tutorialspoint.com/csharp/csharp_interfaces.htm)

Defina una interfaz mediante la palabra clave **interface**

```
public interface ITransactions {
   // interface members
   void showTransaction();
   double getAmount();
}
```

Por convención, los nombres de interfaz comienzan con una letra **I** mayúscula.

---
###### Ejemplos
```
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System;

namespace InterfaceApplication {
   
   public interface ITransactions {
      // interface members
      void showTransaction();
      double getAmount();
   }
   public class Transaction : ITransactions {
      private string tCode;
      private string date;
      private double amount;
      
      public Transaction() {
         tCode = " ";
         date = " ";
         amount = 0.0;
      }
      public Transaction(string c, string d, double a) {
         tCode = c;
         date = d;
         amount = a;
      }
      public double getAmount() {
         return amount;
      }
      public void showTransaction() {
         Console.WriteLine("Transaction: {0}", tCode);
         Console.WriteLine("Date: {0}", date);
         Console.WriteLine("Amount: {0}", getAmount());
      }
   }
   class Tester {
     
      static void Main(string[] args) {
         Transaction t1 = new Transaction("001", "8/10/2012", 78900.00);
         Transaction t2 = new Transaction("002", "9/10/2012", 451900.00);
         
         t1.showTransaction();
         t2.showTransaction();
         Console.ReadLine();
      }
   }
}
```
---
###### Ejemplos
```
    class Program
    {
        public interface INotifications
        {
            void showNotifications();
            string getDate();
        }

        public class NotificationEspañol : INotifications
        {
            private string sender;
            private string message;
            private string date;

            public NotificationEspañol(string mySender, string myMessage, string myDate)
            {
                this.sender = mySender;
                this.message = myMessage;
                this.date = myDate;
            }

            public void showNotifications()
            {
                Console.WriteLine("Message {0} - was sent by {1} - at {2}", message, sender, date);
            }

            public string getDate()
            {
                return date;
            }
        }

        public class Notification : INotifications
        {
            private string sender;
            private string message;
            private string date;

            public Notification()
            {
                sender = "Admin";
                message = "Yo, what's up?";
                date = "";
            }

            public Notification(string mySender, string myMessage, string myDate)
            {
                this.sender = mySender;
                this.message = myMessage;
                this.date = myDate;
            }

            public void showNotifications()
            {
                Console.WriteLine("Message {0} - was sent by {1} - at {2}", message, sender, date);
            }

            public string getDate()
            {
                return date;
            }
        }

        static void Main(string[] args)
        {
            Notification n1 = new Notification("Denis", "Tsup bro?","12.06.2018");
            Notification n2 = new Notification("Frank", "All good", "12.06.2018");
            NotificationEspañol n3 = new NotificationEspañol("Milton", "Hola hermano", "19092018");
            NotificationEspañol n4 = new NotificationEspañol("Charly", "Hola todo bien", "19092018");

            n1.showNotifications();
            n2.showNotifications();
            n3.showNotifications();
            n4.showNotifications();

            Console.ReadLine();
        }
    }
```
---
##### [Implementación de interfaces](https://docs.microsoft.com/es-mx/dotnet/csharp/programming-guide/interfaces/)

Resumen de interfaces

Una interfaz tiene las propiedades siguientes:

* Una interfaz es como una clase base abstracta. Cualquier clase o estructura que implementa la interfaz debe implementar todos sus miembros.
* No se puede crear una instancia de una interfaz directamente. Sus miembros se implementan por medio de cualquier clase o estructura que implementa la interfaz.
* Las interfaces pueden contener eventos, indizadores, métodos y propiedades.
* Las interfaces no contienen ninguna implementación de métodos.
* Una clase o estructura puede implementar varias interfaces. Una clase puede heredar una clase base y también implementar una o varias interfaces.

---
### *Examen 3 09/25/2018* 

			###### Descargue y genere un proyecto nuevo con el siguiente código [link](https://github.com/MarcoZmpk/UNAM_FI_TDP_2018/tree/master/Examen3) 
			###### El objetivo es utilizar leer desde nuestra aplicación los archivos txt y mostrar la información indicada por el profesor en un DataGrid
			###### Al terminar el examen subir el programa a un repositorio personal y los resultados de las pruebas en un archivo txt a un repositorio personal llamado *Examenes*
			###### Enviar el link al repositorio mediante el classroom de google.
---
#### [Manejadores de eventos](https://docs.microsoft.com/es-es/dotnet/standard/events/)

Los eventos de .NET Framework se basan en un modelo de delegado. El modelo de delegado sigue el patrón de diseño del observador, que permite que un suscriptor se registre con un proveedor y reciba notificaciones de dicho proveedor. El emisor de un evento inserta una notificación de que se ha producido un evento, y un receptor de eventos recibe la notificación y define una respuesta a la misma.

---
#### [Evento](https://docs.microsoft.com/es-es/dotnet/standard/events/)

Un evento es un mensaje que envía un objeto cuando ocurre una acción. La acción podría ser debida a la interacción del usuario, como hacer clic en un botón, o podría proceder de cualquier otra lógica del programa, como el cambio del valor de una propiedad. El objeto que provoca el evento se conoce como emisor del evento. El emisor del evento no sabe qué objeto o método recibirá (controlará) los eventos que genera
---
#### [Evento](https://docs.microsoft.com/es-es/dotnet/standard/events/)
- Para definir un evento, se utiliza la palabra clave **event** en la signatura de la clase de eventos y se especifica el tipo de delegado para el evento

```
Normalmente, para generar un evento, se agrega un método marcado como protected y virtual (en C#). Asigne a este método el nombre OnEventName; por ejemplo, OnDataReceived.

El método debe tomar un parámetro que especifica un objeto de datos de evento. Este método se proporciona para permitir que las clases derivadas reemplacen la lógica para generar el evento. Una clase derivada siempre debería llamar al método OnEventName de la clase base para asegurarse de que los delegados registrados reciben el evento.
```
---
#### [Controladores de eventos](https://docs.microsoft.com/es-es/dotnet/standard/events/)

Para responder a un evento, se define un método controlador de eventos en el receptor de eventos. Este método debe coincidir con la signatura del delegado del evento que se está controlando. En el controlador de eventos, se realizan las acciones que es necesario llevar a cabo cuando se genera el evento, como recopilar los datos proporcionados por el usuario cuando este hace clic en un botón. Para recibir notificaciones cuando se genera el evento, el método controlador de eventos debe suscribirse al evento
---
###### Ejemplos
```
namespace RaisingEvents
{
    public partial class Form1 : Form
    {
        int counter = 0;
        Boolean limit = false;
        Contador c = new Contador(4);

        public Form1()
        {
            InitializeComponent();
            c.ThresholdReached += c_ThresholdReached;
        }

        private void button1_Click(object sender, EventArgs e)
        {
            counter++;
            c.Add(counter);
            if (limit)
            {
                if (counter < 5)
                {
                    textBox1.Text = counter.ToString();

                }
                else
                {
                    textBox1.Text = 5.ToString();
                    counter = 5;
                }
            }
            else
            {
                if (counter < 10)
                {
                    textBox1.Text = counter.ToString();
                }
                else
                {
                    textBox1.Text = 10.ToString();
                    counter = 10;
                }
            }           
        }

        private void trackBar1_Scroll(object sender, EventArgs e)
        {
            textBox1.Text = trackBar1.Value.ToString();
            counter = trackBar1.Value;
            c.Add(counter);
            if (counter < 4)
            {
                this.pictureBox1.Image = Properties.Resources.Green;
            }
        }

        private void checkBox1_CheckedChanged(object sender, EventArgs e)
        {
            limit = checkBox1.Checked;
            if (limit)
            {
                trackBar1.Maximum = 5;
            }
            else
            {
                trackBar1.Maximum = 10;
            }
        }

        private void button1_MouseClick(object sender, MouseEventArgs e)
        {
            trackBar1.Value = counter;
        }

        public void c_ThresholdReached(object sender, EventArgs e)
        {
            this.pictureBox1.Image = Properties.Resources.alert;
        }

    }
	
	class Contador
    {
        private int threshold;

        public event EventHandler ThresholdReached;

        public Contador(int passedThreshold)
        {
            threshold = passedThreshold;
        }

        public void Add(int x)
        {
            if (x >= threshold)
            {
                OnThresholdReached(EventArgs.Empty);
            }
        }

        protected virtual void OnThresholdReached(EventArgs e)
        {
            EventHandler handler = ThresholdReached;
            if (handler != null)
            {
                handler(this, e);
            }
        }
    }
}
```
---
### Questions?

<br>

@fa[envelope gp-contact](zmpk.fi@gmail.com)

@fa[github gp-contact](MarcoZmpk)

---
#### Construcción de bibliotecas y reutilización de código

---
#### Almacenamiento, actualización y eliminación de información en base a estructuras

---
#### Manejo de archivos (escritura, lectura, acceso secuencial, acceso aleatorio)

---
### 3. Desarrollo de sistemas de cómputo orientados a objetos

<br>

#### Objetivo:
#### 

---

### 4. Concepto, uso y aplicaciones de las estructuras de datos compuestas

<br>

#### Objetivo:
#### 

---

### 5. Interfaces gráficas de usuario

<br>

#### Objetivo:
#### 
---


### Questions?

<br>

@fa[envelope gp-contact](zmpk.fi@gmail.com)

@fa[github gp-contact](MarcoZmpk)

---
#### Referencias
---
