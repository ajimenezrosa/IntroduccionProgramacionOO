|ANALISIS Y DISENO |DE ALGORITMOS|
|---------------------|------------------------|
|![](https://avatars.githubusercontent.com/u/7384546?v=4)|![](https://pbs.twimg.com/profile_images/901546652091252736/6Clcdv1L_400x400.jpg)|
# 8 Ejercicios resueltos con el ciclo while en C#
#### 

#### En esta ocasión, y para reforzar los conocimientos del ciclo while, he creado una serie de 8 ejercicios para que practiques las habilidades aprendidas.

#### Si en dado caso, tienes problemas para resolver alguno, he adjuntado la correspondiente respuesta para que puedas guiarte.



##### 1 1. [Realiza un programa en C#, que muestre los primeros 100 números enteros iniciando desde el 1](#ejer1)
##### 2 2.- [Realiza un programa en C#, que muestre los primeros 100 números de forma inversa, es decir, del 100 al 1](#ejer2)
##### 3 3.- [Realiza un programa en C#, que muestre únicamente, los números pares en el rango del 1 al 100](#ejer3)
##### 4 4.- [Realiza un programa en C#, que muestre la suma de los números del 1 al 100](#ejer4)
##### 5 5.- [Realiza un programa en C#, que muestre la suma de los números impares del 1 al 100](#ejer5)
##### 6 6.- [Realiza un programa en C#, que pida números mientras no se ingrese uno negativo. Al final, se debe mostrar la suma de los números ingresados](#ejer6)
##### 7 7.- [Realiza un programa en C#, que muestre un menú en pantalla con las opciones:1) Sumar2) Restar3) Multiplicar4) Dividir5) SalirEl usuario debe seleccionar una opción. y a continuación, el programa deber solicitar el ingreso de 2 números enteros. Una vez ingresados los números, se deberá evaluar con un switch, realizando la operación correspondiente a la opción seleccionada.La ejecución debe realizarse una y otra vez, hasta que el usuario seleccione la opción # 5.](#ejer7)
##### 8 8.- [Realiza un programa en C#, que pida 2 números enteros, e imprima los números pares que existen entre los 2.Nota: Se debe validar que el segundo número sea mayor que el primero.](#ejer8)

#### 9 - [Metodos](#metodos)

#### 1.- Realiza un programa en C#, que muestre los primeros 100 números enteros iniciando desde el 1.<a name="ejer1"></a>
~~~c#
using System;
class Program
{
    static void Main(string[] args)
    {
        int contador = 1;
        while (contador <= 100)
        {
            Console.WriteLine(contador);
            contador += 1;
        }
    }
}
~~~


#### 2.- Realiza un programa en C#, que muestre los primeros 100 números de forma inversa, es decir, del 100 al 1<a name="ejer2"></a>
~~~C#
using System;
class Program
{
    static void Main(string[] args)
    {
        int contador = 100;
        while (contador >= 1)
        {
            Console.WriteLine(contador);
            contador -= 1;
        }
    }
}
~~~
#### 3.- Realiza un programa en C#, que muestre únicamente, los números pares en el rango del 1 al 100 <a name="ejer3"></a>
~~~C#
using System;
class Program
{
    static void Main(string[] args)
    {
        int contador = 1;
        while (contador <= 100)
        {
            if (contador % 2 == 0)
            {
                Console.WriteLine(contador);
            }
            contador += 1;
        }
    }
}
~~~
#### 4.- Realiza un programa en C#, que muestre la suma de los números del 1 al 100 <a name="ejer4"></a>
~~~C#
using System;
class Program
{
    static void Main(string[] args)
    {
        int contador = 1;
        int suma = 0;
        while (contador <= 100)
        {
            suma += contador;
            contador += 1;
        }
        Console.WriteLine($"La suma es {suma}");
    }
}
~~~
#### 5.- Realiza un programa en C#, que muestre la suma de los números impares del 1 al 100<a name="ejer5"></a>
~~~C#
using System;
class Program
{
    static void Main(string[] args)
    {
        int contador = 1;
        int suma = 0;
        while (contador <= 100)
        {
            if (contador % 2 != 0)
            {
                suma += contador;
            }
            contador += 1;
        }
        Console.WriteLine($"La suma es {suma}");
    }
}
~~~

#### 6.- Realiza un programa en C#, que pida números mientras no se ingrese uno negativo. Al final, se debe mostrar la suma de los números ingresados<a name="ejer6"></a>
~~~C#
using System;
class Program
{
    static void Main(string[] args)
    {
        int suma = 0;
        int ingresado = 0;
        while (ingresado >= 0)
        {
            suma += ingresado;
            Console.WriteLine("Ingresar número: ");
            ingresado = int.Parse(Console.ReadLine());
        }
        Console.WriteLine($"La suma es {suma}");
    }
}
~~~

#### 7.- Realiza un programa en C#, que muestre un menú en pantalla con las opciones:<a name="ejer7"></a>

1) Sumar
2) Restar
3) Multiplicar
4) Dividir
5) Salir

El usuario debe seleccionar una opción. y a continuación, el programa deber solicitar el ingreso de 2 números enteros. Una vez ingresados los números, se deberá evaluar con un switch, realizando la operación correspondiente a la opción seleccionada.
La ejecución debe realizarse una y otra vez, hasta que el usuario seleccione la opción # 5.
~~~C#
using System;
using System.Security.Cryptography;
class Program
{
    static int numero1 = 0;
    static int numero2 = 0;
    static void Main(string[] args)
    {
        int opcion = 0;
        bool debeCorrer = true;
        while (debeCorrer)
        {
            Console.WriteLine("Seleccione una opción de la Lista:");
            Console.WriteLine("1.- Sumar");
            Console.WriteLine("2.- Restar");
            Console.WriteLine("3.- Multiplicar");
            Console.WriteLine("4.- Dividir");
            Console.WriteLine("5.- Salir");
            opcion = int.Parse(Console.ReadLine());
            switch (opcion)
            {
                case 1: SolicitarNumeros();
                    Console.WriteLine($"El resultado es {numero1 + numero2}");
                    break;
                case 2: SolicitarNumeros();
                    Console.WriteLine($"El resultado es {numero1 - numero2}");
                    break;
                case 3: SolicitarNumeros();
                    Console.WriteLine($"El resultado es {numero1 * numero2}");
                    break;
                case 4: SolicitarNumeros();
                    Console.WriteLine($"El resultado es {numero1 / numero2}");
                    break;
                case 5:
                    debeCorrer = false;
                    break;
            }
        }
    }
    static void SolicitarNumeros()
    {
        Console.WriteLine("Ingrese número 1: ");
        numero1 = int.Parse(Console.ReadLine());
        Console.WriteLine("Ingrese número 2: ");
        numero2 = int.Parse(Console.ReadLine());
    }
}
~~~
#### 8.- Realiza un programa en C#, que pida 2 números enteros, e imprima los números pares que existen entre los 2.<a name="ejer8"></a>

Nota: Se debe validar que el segundo número sea mayor que el primero.
~~~C#
using System;
using System.Security.Cryptography;
class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Ingrese número 1: ");
        var numero1 = int.Parse(Console.ReadLine());
        Console.WriteLine("Ingrese número 2: ");
        var numero2 = int.Parse(Console.ReadLine());
        if (numero1 > numero2)
        {
            Console.WriteLine("El número 2 debe ser mayor que el número 1");
            return;
        }
        int contador = numero1;
        while (contador <= numero2)
        {
            if (contador % 2 == 0)
            {
                Console.WriteLine(contador);
            }
            contador++;
        }
    }
}
~~~


#
# Metodos<a name="metodos"></a>

#### Un método en C# es una sencuencia de enunciados dentro de una unidad lógica en nuestro programa. Son una de las partes escenciales en cualquier aplicación, y proporcionan una forma poderosa de ejecutar operaciones de forma ordenada.

#

#### 
Video sobre la creación y uso de Métodos en C#

# 

## Partes de un Método en C#
#### Si deseamos aprender cómo crear un método, debemos de considerar 4 partes a recordar:

    Un nombre significativo
    Los enunciados que se ejecutarán cuando se invoque el método
    Un único tipo de dato de retorno
    Uno ó más datos de entrada, con los que nuestro método puede funcionar (Opcional).

## Sintaxis de un Método en C#
#### La sintaxis fundamental para crear un método, es la siguiente:
~~~C#
tipoRetorno nombreMetodo (ListaDeParámetros)
{
   //Enunciados que se ejecutarán
}
~~~
###### Como puedes apreciar en el código anterior, he escrito cada uno de los elementos de la lista, a continuación, describiré cada uno de los elementos.

#### Como puedes apreciar en el código anterior, he escrito cada uno de los elementos de la lista, a continuación, describiré cada uno de los elementos.
# 

#### nombreMetodo -> Nombre significativo del método: Este es el nombre con el que invocaremos el método desde otras partes de nuestro programa, se recomienda que tenga un nombre significativo, que denote una acción, es decir, que sea un verbo. Un ejemplo podría ser “DibujarCuadrado”, ó “CalcularArea”. Cabe destacar, que el nombramiento de los métodos, sigue las mismas reglas que el nombramiento de variables.
#

#### ListaDeParametros -> Datos de entrada: Estos representan información que podemos pasar a nuestro método, con el fin de que los enunciados dentro de él, puedan trabajar con dicha información. Se tienen que escribir dentro de un par de paréntesis, y la sintaxis para declarar estos parámetros, es: “tipoDeDato” + “nombreParametro”. En dado caso de que deseemos declarar más de un parámetro, tendremos que separarlos con una coma (,).

#
#### Enunciados que se ejecutarán:  Son el conjunto de enunciados que realizrán operaciones dentro de nuestro método cuando éste sea invocado. Se tienen que escribir dentro de las llaves del método ({}).

## **Ejemplos**
#### Vamos a ver algunos ejemplos prácticos para que quede completamente claro el concepto de métodos:
~~~C#
void Imprimir()
{
   Console.WriteLine("Hola Mundo!");
}
~~~
#### En el ejemplo anterior, el método no regresará ningún valor, se llama Imprimir, no acepta ningún valor como parámetro y se encargará de Imprimir un Hola Mundo en la pantalla del usuario.
# 
#### En dado caso de que queramos que el método, imprima una cadena, pero personalizada, podremos agregar un parámetro, para enviar desde otra parte de nuestro programa una cadena, y así el resultado sea diferente:
~~~C#
void Imprimir(string nombre)
{
   Console.WriteLine("Hola " + nommbre);
}
~~~
#
#### En el ejemplo anterior, el método no regresará ningún valor, se llama Imprimir, no acepta ningún valor como parámetro y se encargará de Imprimir un Hola Mundo en la pantalla del usuario.
#
#### En dado caso de que queramos que el método, imprima una cadena, pero personalizada, podremos agregar un parámetro, para enviar desde otra parte de nuestro programa una cadena, y así el resultado sea diferente:
~~~C#
void Imprimir(string nombre)
{
   Console.WriteLine("Hola " + nommbre);
}
~~~
#### Con esta modificación, el método sigue sin regresar ningún valor, pero hemos agregado a la lista de parámetros, uno que se llama nombre, el cual almacenará el resultado en la variable nombre. Utilizaremos dicho valor más adelante para imprimir en consola, Hola + el valor que enviemos a la variable nombre.

#### Supongamos que ahora deseamos que nuestro método, aparte de imprimir “Hola Héctor” (suponiendo que ese valor tiene la variable nombre), también deseamos regresar dicha cadena al  lugar desde donde fue invocado el método. Esto lo podríamos lograr, modificando nuestro método, indicando que deseamos regresar una cadena de texto:

~~~C#
string Imprimir()
{
   Console.WriteLine("Hola Mundo!");
}
~~~
#### Como te habrás dado cuenta, hemos cambiado el void por el string, lo que nos permitirá retornar la cadena de texto que queremos.
#
#### Vamos a ver otros ejemplos, que con el conocimiento adquirido, seguro podremos interpretar fácilmente:
~~~C#
int Sumar(int numero1, int numero2)
{
    //Enunciados a ejecutar
}
~~~
#
#### En el ejemplo anterior, estamos indicando que deseamos regresar un número entero, el método se llama Sumar (bastante representativo), y recibe 2 parámetros enteros, donde almacenaremos los valores de 2 números enteros, para posteriormente ejecutar una ó más operaciones.
#
## ¿Cómo regresar un valor de un método en C#?
#### Si en dado caso, deseamos regresar un valor, como resultado de la ejecución de uno ó más enunciados de nuestro método, podremos hacerlo a través de la siguiente sintaxis:
~~~C#
return ValorARegresar;
~~~
#
#### La palabra return es fundamental para llevar a cabo dicha operación, ya que será la que nos indique que deseamos regresar el valor que le sigue. Tomemos como ejemplo, el código anterior de este punto, y agreguemos un return:
~~~C#
int Sumar(int numero1, int numero2)
{
     return numero1 + numero2;
}
~~~
#
#### Hemos agregado la palabra clave return, y finalmente, una operación, la que llevará a cabo la suma de numero1 + numero2. Dicho return, podría regresar el resultado final de un conjunto de operaciones, pero siempre será un único valor.
#
#### De igual forma, es importante destacar que una vez invocado el enunciado con return, el código siguiente ya no se ejecutará, por lo que hay que tener cuidado de ver bien dónde lo utilizaremos.
#
#### Otro punto importante a denotar, es que podemos utilizar la palabra clave return sin ningún valor adicional, esto podría considerarse un tipo si en dado caso queremos cortar la ejecución de una función en dado caso de que se cumpla una condición, por ejemplo:
~~~C# 
bool VerificarEdad(int edad)
{
   if(edad &lt; 18)
   {
      return;
   }
   //Ejecutar enunciados si es mayor de edad
}
~~~

## Métodos de Expresión Corporal (Expression Bodied Methods)

#### Existen ocasiones, en las que deseamos ejecutar alguna operación sencilla, o bien, una única operación en nuestro código, por lo que no deseamos declarar un método completo, ya que esto podría suponer la creación de mucho código.
#
#### Afortunadamente, en C#, contamos con una forma simplificada de escribir dichos métodos, que al igual que un método normal, nos permite retornar un tipo de dato, y a la vez, pasar parámetros.
#
#### La definición de estos métodos, es de la siguiente forma:
#
#### TipoDatoRetorno NombreMetodo(parámetros) => EnunciadoAEjecutar
#
#### He marcado en negritas el símbolo que representa este tipo de métodos, ya que será el que utilicemos en lugar del par de llaves que se usa normalmente.
#
#### Por ejemplo, si deseamos reescribir el método que realiza la suma entre dos valores, que hemos escrito anteriormente, lo haríamos de la siguiente forma:

~~~C#
int Sumar(int numero1, int numero2) => return numero1 + numero2;
~~~
#### Como puedes observar, aparte del uso del símbolo =>, también estamos eliminando el uso de la palabra clave return, ya que en este tipo de expresiones no es necesaria. El valor de la expresión, será automáticamente devuelto.
#
#### Por otra parte, si el método no da como resultado el retorno de un valor, entonces, se inferirá que es de tipo void, como en el siguiente ejemplo:
~~~C#
void hello() => Console.WriteLine("Hola Mundo!);
~~~
# 
#### En realidad, no hay ventaja en cuanto a rendimiento entre utilizar la definición normal de un método, ó bien, un método de expresión corporal, sino que únicamente nos servirán para reducir la cantidad de llaves ({}) en nuestro programa.

## ¿Cómo invocar un método en C#?
#### Ya anteriormente hemos visto cómo declarar un método, sin embargo, hay que saber cómo invocarlo desde nuestro programa.
#
#### En primer lugar, iniciaremos colocando en Visual Studio, en un proyecto de consola, uno de los métodos definidos anteriormente:

~~~C#
using System;
using System.collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Task;

namespace ConsoleTests
{
    class Program
    {

        static void Main(string[] args)
        {

        }

        void Imprimir()
        {
            Console.WriteLine("Hola Mundo!")
        }

    }

}
~~~


## practica de metodos
~~~C#
// See https://aka.ms/new-console-template for more information
//Console.WriteLine("Hello, World!");


//Console.WriteLine("Hola");
//Console.WriteLine("Hola 2");

//Console.ReadLine();

//Console.WriteLine("Hola");
//Console.WriteLine("Hola 2");

//Console.ReadLine();
Console.ReadKey();
//Imprimir();

//Imprimir2("Ricardo");
//Imprimir2("Jose Angel");


Imprimir2(
    retornarString("Alejandro")
    );

static void Imprimir()
{
    Console.Clear();
    Console.WriteLine("Hola 1");
    Console.WriteLine("Hola 2");
    Console.ReadLine();
}


// metodo con  parametros
static void Imprimir2(string nombre )
{
    Console.Clear();
    Console.WriteLine("Hola " + nombre);
    Console.ReadKey();
}



 string retornarString(string nombre)
{
    nombre = Console.ReadLine();
    return "Retorno de valor " + nombre;
}

~~~




