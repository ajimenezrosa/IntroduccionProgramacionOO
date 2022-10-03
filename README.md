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
#### 10 - [Excepciones](#Excepciones)
#### 10.1 - [El método Parse](#parse)



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

#
# Excepciones<a name="Excepciones"></a>
#### Es algo muy común en una aplicación que desarrolle las cosas salen mal y es que muchas veces una pieza de código puede fallar debido a múltiples razones.

#### Por lo que debemos asegurarnos de que nuestra aplicación pueda manejar dichas fallas o en el peor de los casos notificar al usuario sobre el problema lo más claramente posible esto lo podemos hacer A través de las excepciones.
# 
#### Para ver este tema de forma práctica vamos a crear un nuevo proyecto entonces seleccionamos nuevo proyecto aplicación de consola net framework que vamos a ponerle ***excepciones1demos***

Colocamos el Siguiente Codigo
~~~C#
    int valor - 10;
    Console.WriteLine(valor / 0);
~~~

#### No es posible dividir entre cero , esto deberia darnos un error.
    Excepcion no controlada
    System.DivideByZeroException: 'Intento dividir por cero'



## El método Parse<a name="parse"></a>
#### Una forma de minimizar los errores en nuestro programa es la siguiente.

#### Podemos convertir cadenas de texto en números utilizando el método de análisis.
# 
~~~C#
    string numeroEnCadena = "10";
    int valor = int.Parse(NumeroEnCadena);

    Console.WriteLine(valor);

    Console.ReadLine();
~~~



## Estructura try-catch
#### La instrucción try-catch consta de un bloque try seguido de una o más cláusulas catch que especifican controladores para diferentes excepciones.
# 
#### Cuando se produce una excepción, Common Language Runtime (CLR) busca la instrucción catch que controla esta excepción. Si el método que se ejecuta actualmente no contiene un bloque catch, CLR busca el método que llamó el método actual, y así sucesivamente hasta la pila de llamadas. Si no existe ningún bloque catch, CLR muestra al usuario un mensaje de excepción no controlada y detiene la ejecución del programa.


#### Codigo C#
~~~C#
string numeroGrande = "999999999";
int numeroConvertido = int.Parse(NumeroGrande);

Console.WriteLIne(NumeroConvertido);

Console.ReadLine();
~~~

    Para el caso del ejemplo anterior podemos ver que funciona correctamente, imprimirá 999999999.

    Pero si hace la prueba y agrega otro número 9 a la lista, esto dará un error.

    Este tipo de errores son los que debemos controlar usando nuestras excepciones.

#### Estos son los errores con los que nosotros, como programadores, debemos aprender a lidiar.

#### para esto usaremos una estructura llamada try-catch
#### las estructura es la siguiente:
    try
    {
         Operaciones que queremos llevar a cabo con comprobaciones
    }
    catch(Tipo de Excepcion ex)
    {
        Operaciones que se ejecutaran en dado caso de que ocurra una excepcion
    }

#### Siguiendo esta plantilla que tenemos aquí procederemos a crear este código en c#

~~~C#

    //Ejemplo #2
    try
    {
         int valor - 10;
         Console.WriteLine(valor / 0);
    }
    catch(DivideByZeroException ex)
    {
        Console.WriteLine("No se puede dividir entre cero");
    }


    //Ejemplo #2
    try
    {
        string numeroEnCadena = '1a';
        int valor2 = int.Parse(numeroEnCadena);
    }
    catch(DivideByZeroException ex)
    {
        Console.WriteLine("No se Puede dividir por Cero");
    }
    catch(FormatException ex)
    {
        Console.WriteLine("Unicamente se Aceptan Numeros");
    }

    // Ejemplo #3

    try
    {
        string numeroGrande = "999999999";
        int numeroConvertido = int.Parse(numeroGrande);
    }
    catch(DivideByZeroException ex)
    {
        Console.WriteLine("No se Puede dividir por Cero");
    }
    catch(FormatException ex)
    {
        Console.WriteLine("Unicamente se Aceptan Numeros");
    }
    catch(OverflowException ex)
    {
        //En este caso utilizaremos el valor de la variable message.
        Console.WriteLine(ex.Message);
    }


~~~

#### Este sería un buen ejemplo de cómo se manejan las excepciones en C#.

## Tipos de Excepciones.

#### Al ver esto te debes estar preguntando: **¿Necesito aprender cada uno de los tipos de excepción que existen en C#?**

### ***¡¡Bueno en realidad no!!***

#### En el lenguaje C# tenemos un tipo de excepción especial que maneja todos los tipos de excepciones que no estamos manejando a través de capturas.

    Ejemplo 
~~~c#
        string s = null; // For demonstration purposes.

        try
        {
            ProcessString(s);
        }
        catch (Exception e)
        {
            Console.WriteLine("{0} Exception caught.", e);
        }
~~~        


## Chequeo de Operaciones Aritmeticas a travez de **checked**


#### Usamos el siguiente código como un ejemplo del uso de marcado para la validación de enteros.
~~~C#
    // esto me asigna el valor maximo de int a la variable entero
    int entero = int.MaxValue;

    // incremento en uno este valor
    entero++;

    Console.WriteLine(entero);
    console.ReadLine();
~~~

#### Como puedes ver, al ejecutar este código, no presenta ningún error en el programa.

#### Pero los datos presentados por él son incorrectos. Esto se debe a que las operaciones con enteros son muy comunes y es muy costoso verificar operación por operación.

#### para este tipo de casos usaremos el marcado

~~~C#

    // esto me asigna el valor maximo de int a la variable entero
    int entero = int.MaxValue;

    checked {
        // incremento en uno este valor
        entero++;
    }

    Console.WriteLine(entero);
    console.ReadLine();

~~~

en este caso presenta un excepcion **OverflowException**

#### Otra forma de que esto funciones es la siguiente.
~~~c#
    entero = checked(entero++);
~~~

#### Para saltarnos esta validacion colocamos un **unchecked** en el codigo en vez de **checked**

### Nota: con un **unchecked** el error no se presentara debido anulamos la verificacion.  pero debemos tener en claro que el dato que retorna puedo o no se correcto. 
#

## Lanzando Excepciones a proposito.
#
Para este ejemplo utilizarmos el suguiente codigo


~~~C#

    static string obternerSignoZodiacal(int numeroMes)
    {
    string resultado = string.Empty;
        switch(numeroMes)
        {
            case 1:
                resultado = "Aries";
                break;
            case 1:
                resultado = "Tauro";
                break;
            case 1:
                resultado = "Geminis";
                break;
            case 1:
                resultado = "Cancer";
                break;
            case 1:
                resultado = "leo";
                break;
            case 1:
                resultado = "Virgo";
                break;
            case 1:
                resultado = "Libra";
                break;
            case 1:
                resultado = "Escorpion";
                break;
            case 1:
                resultado = "Sagitario";
                break;
            case 1:
                resultado = "Capricornio";
                break;
            case 1:
                resultado = "Acuario";
                break;
            case 1:
                resultado = "Pisis";
                break;
        }

    return resultado;

    }
~~~

#### Luego de esto procederemos a llamar a nuestro método para que muestre el signo zodiacal que corresponde al mes en cuestión.

~~~C#
    int mes int.Parse(Console.ReadLine());

    Console.WriteLine(ObtenerSignoZodiacal(mes));
    
    Console.ReadLine();
~~~

#


#### Para este código, qué pasaría si al ejecutar la aplicación ingresé el mes número 50, por ejemplo.


#### En nuestro caso, debemos lanzar una excepción para que se sepa que el dato suministrado no es el esperado.
   en este caso usaremos la expresión **default** en nuestro **switch**.

    default:
        throw new InvalidOperationException("Mes Invalido");

~~~C#

    static string obternerSignoZodiacal(int numeroMes)
    {
    string resultado = string.Empty;
        switch(numeroMes)
        {
            case 1:
                resultado = "Aries";
                break;
            case 1:
                resultado = "Tauro";
                break;
            case 1:
                resultado = "Geminis";
                break;
            case 1:
                resultado = "Cancer";
                break;
            case 1:
                resultado = "leo";
                break;
            case 1:
                resultado = "Virgo";
                break;
            case 1:
                resultado = "Libra";
                break;
            case 1:
                resultado = "Escorpion";
                break;
            case 1:
                resultado = "Sagitario";
                break;
            case 1:
                resultado = "Capricornio";
                break;
            case 1:
                resultado = "Acuario";
                break;
            case 1:
                resultado = "Pisis";
                break;
            default :
                throw new InvalidOperationException("Mes Invalido")    
            }

            return resultado;

    }
~~~



con esto colocamos un try catch al momento de ejecutar nuestro método.

~~~C#
    int mes = int.Parse(Console.ReadLine());

    try
    {
        console.WriteLine(OptenerSignoZodiacal(mes));
    }
    catch(Exception ex)
    {
        Console.WriteLine(ex.Message);
    }
~~~

Ejecute la aplicación e ingrese un mes que no existe
