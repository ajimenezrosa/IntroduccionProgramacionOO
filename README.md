|Alejandro Jimenez |UCSD|
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
#### 10.2 - [Estructura try-catch](#trycatch)
#### 10.3 - [Tipos de Excepciones.](#TiposExceptiones)
#### 10.4 - [Chequeo de Operaciones Aritmeticas a travez de **checked**](#checked)
#### 10.5 - [Lanzando Excepciones a proposito.](#lanzarExceptiones)

#### 10.7   [Ejercicios para el Aula](#EjercicioMetodoExcepciones)


#### 10.8   [Practica #2 Metodos y Excepciones.](#EjercicioMetodoExcepciones2)


#### [11 - Clases y Objetos](#objetosClases)
#### [11.1 - Pilares de Poo](#pilares)
#### [11.2 - Que es una Clase](#clases)

#

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



## Estructura try-catch<a name="trycatch"></a>
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

## Tipos de Excepciones.<a name="TiposExceptiones"></a>

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


## Chequeo de Operaciones Aritmeticas a travez de **checked**<a name="checked"></a>


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

## Lanzando Excepciones a proposito.<a name="lanzarExceptiones"></a>
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




## Ejercicios para el Aula<a name="EjercicioMetodoExcepciones"></a>
#### Haz este ejercicio en el salón de clases:
#### Trate de no copiar, escriba los comandos y de esta manera se familiarizará con ellos.
#

#
## Haz tu práctica:

### Recuerda que la perseverancia es la clave del éxito;
### Fíjate bien dónde pones los comandos; no hagas una copia del código. Tu principal objetivo es aprender, recuerda que este conocimiento te servirá mañana en tu vida profesional.

## Mantén viva tu curiosidad pregunta, investiga



~~~C#
using System;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Dias de la Semana!");
            Console.WriteLine("Digite el dia de la Semana(Solo Numeros):");
            int valor = int.Parse(Console.ReadLine());

            Console.WriteLine(
                    DiasDeLaSemana(valor)
                );

        }


        /* Como puedes ver la Declaracion del metodo **DiasDeLaSemana** esta fuera del static void Main(string[] args) 

        pero para llamarlo lo hacemos desde dentro del static void Main(string[] args)

        Nota: Si tienes Visual Studio 2022 no tendras que colocar el static void Main(string[] args)

            */
        static string DiasDeLaSemana(int dia)
        {
            string resultado = "";
            switch (dia)
            {
                case 1:
                    resultado = "Lunes";
                    break;
                case 2:
                    resultado = "Martes";
                    break;
                case 3:
                    resultado = "Miercoles";
                    break;
                case 4:
                    resultado = "Jueves";
                    break;
                case 5:
                    resultado = "viernes";
                    break;
                case 6:
                    resultado = "Sabado";
                    break;
                case 7: resultado = "Domingo";
                    break;

            }

            return resultado;


        }


    }
}

~~~


Ahora haremos la segunda parte del Ejercicio:

A este mismo código le colocaremos el Try-Catch para el manejo de excepciones.
Lo primero que debemos hacer es generar una excepción en el programa.
Si tiene dudas, lea nuevamente.
#
#### 10.2 - [Estructura try-catch](#trycatch)
#### 10.3 - [Tipos de Excepciones.](#TiposExceptiones)
#### 10.4 - [Chequeo de Operaciones Aritmeticas a travez de **checked**](#checked)
#### 10.5 - [Lanzando Excepciones a proposito.](#lanzarExceptiones)

#
~~~C#

        static string DiasDeLaSemana(int dia)
        {
            string resultado = "";
            switch (dia)
            {
                case 1:
                    resultado = "Lunes";
                    break;
                case 2:
                    resultado = "Martes";
                    break;
                case 3:
                    resultado = "Miercoles";
                    break;
                case 4:
                    resultado = "Jueves";
                    break;
                case 5:
                    resultado = "viernes";
                    break;
                case 6:
                    resultado = "Sabado";
                    break;
                case 7: resultado = "Domingo";
                    break;
                // Agregamos esta parte del código para probar que el programa devuelve una excepción.
                default:
                    throw new InvalidOperationException("Dia Invalido!");
            }

            return resultado;


        }
~~~

#### Ya casi terminas:
####     Ahora debes colocar el try-catch, este debe estar en la parte del código en la cual llamar a la función.

~~~C#
            try
            {

                Console.WriteLine(
                        DiasDeLaSemana(valor)
                    );
            }
            catch(Exception ex)
            {
                // En este código capturamos la propiedad del Message de la excepción.
                Console.WriteLine(ex.Message);
            }
~~~


## Al final de nuestro código completo se vería así
~~~C#
using System;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Dias de la Semana!");
            Console.WriteLine("Digite el dia de la Semana(Solo Numeros):");
            int valor = int.Parse(Console.ReadLine());


            try
            {

                Console.WriteLine(
                        DiasDeLaSemana(valor)
                    );
            }
            catch(Exception ex)
            {
                // En este código capturamos la propiedad del Message de la excepción.
                Console.WriteLine(ex.Message);
            }


        }

        static string DiasDeLaSemana(int dia)
        {
            string resultado = "";
            switch (dia)
            {
                case 1:
                    resultado = "Lunes";
                    break;
                case 2:
                    resultado = "Martes";
                    break;
                case 3:
                    resultado = "Miercoles";
                    break;
                case 4:
                    resultado = "Jueves";
                    break;
                case 5:
                    resultado = "viernes";
                    break;
                case 6:
                    resultado = "Sabado";
                    break;
                case 7: resultado = "Domingo";
                    break;
                // Agregamos esta parte del código para probar que el programa devuelve una excepción.
                default:
                    throw new InvalidOperationException("Dia Invalido!");
            }

            return resultado;


        }


    }
}

~~~
<!-- ## Practica #2 Metodos y Excepciones. -->

## **Practica #2 Metodos y Excepciones.**<a name="EjercicioMetodoExcepciones2"></a>

#
#### Cree un programa C# que devuelva el día de la semana y el mes a partir de dos entradas numéricas.
#### Valide mediante el manejo de excepciones que el programa no se rompa al recibir un mes o día incorrecto.

#### Tienes un ejemplo a seguir, primero haz el Ejercicio 1:
#### Buena suerte
# 

## Clases y Objetos<a name="objetosClases"></a>

#### la palabra clase es la raíz de la palabra clasificación y es que a menudo solemos utilizar clasificaciones en nuestro día a día.
#### Por ejemplo Fíjate en la imagen tenemos una imagen de un automóvil al verlo seguramente has pensado lo mismo que yo es un automóvil no importa su color marca.
# 
![](https://www.definicionabc.com/wp-content/uploads/autom%C3%B3vil.jpg)

#### Ahora bien porque sabes que es un automóvil y tal vez puedes responderme ***!a porque tiene puertas y llantas!*** bueno veamos la siguiente imagen.
# 
![](https://www.elsoldemexico.com.mx/mexico/sociedad/v4lrel-avion-presidencial-.jpg/ALTERNATES/LANDSCAPE_768/Avio%CC%81n%20presidencial%20.jpg)
#
 #### Lo que aparece la imagen es un automóvil?
 ####  definitivamente no Y eso que un avión también tiene ruedas y puertas si te has fijado en ambos ejemplos podemos sacar algunas conclusiones acerca de que hace que un objeto sea un avión y qué hace que otro sea un automóvil.
 #
 #### En primer lugar tomemos en cuenta las características de cada uno y de otro y esta palabra la quiero recalcar características o en términos de la *programación orientada objetos* **propiedades**, es decir las propiedades que definen al objeto que estamos describiendo.
 #
 ####  En el caso del automóvil una propiedad o característica es que tiene que efectivamente **llantas** 
 #### En el caso del avión también tiene **llantas** nada más que el avión tiene 6 llantas a diferencia del automóvil.
 #
####  Otra característica que comparten los dos objetos son que ambos tienen asientos pero la gran diferencia es el número de asientos que tiene uno contra el otro describiendo un poco más al avión encontramos que tiene alas concretamente 2 alas y está característica es algo que un automóvil no tiene.

#### Que otra característica tiene un avión que no tiene un automóvil un ***par de hélices podría ser otro ejemplo válido*** ahora bien. Vamos a proseguir analizando ambas imágenes pero ahora tomando en cuenta lo que pueden hacer o la funcionalidad que tienen disponible recuerda anteriormente analizamos las características y ahora analizaremos el comportamiento en primer lugar como comportamiento que comparten ambos objetos es el hecho de que los dos pueden avanzar.
|Avion Avanzar| Carro Avanzar|
|-------------|--------------|
|![](https://img.bekia.es/articulos/portada/46000/46368.jpg)|![](https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/genesis-gv80-2021-1600-01-1579079236.jpg)|
#
####  Si te fijas el término lo hemos especificado como una acción  
    avanzar 
#### Otro comportamiento que comparten ambos objetos son que tienen la capacidad de frenar, de nuevo frenar es una acción es decir algo que los dos objetos pueden hacer o llevar a cabo.
#
#### Cuando alguien quiere llevar a cabo dicha acción ahora bien algo en lo que estaremos de acuerdo es que hasta hoy en día aún no existen carros voladores al alcance del público como quisiéramos. Por lo que el único de ambos sujetos que tiene la capacidad de volar es el avión de nuevo ocupamos un verbo para escribir algo que pueda hacer un avión ***volar*** con estas características y comportamientos que hemos visto de cada uno de los objetos podemos llegar a la conclusión de que podemos distinguir un **automóvil** de un **avión** basado en sus **propiedades** y **comportamiento** y que no importando ***Qué modelo de automóvil sea siempre lo clasificaremos como automóvil*** De igual forma pasaría con un avión ***no importa el tamaño o número de motores de un avión para nosotros siempre será un avión*** debido a que ese es la clasificación que le hemos dado en el mundo real es ***por ello que la clasificación es tan importante porque así podemos comunicarnos de forma efectiva*** 
#
### En el mundo de la programación a las ***características se les llama propiedades*** y a los ***comportamientos métodos tema que ya hemos visto anteriormente*** 
#
### Por último el hecho de poder modelar objetos definiendo sus métodos y propiedades se le conoce como programación orientada a objetos.

#

## Pilares de Poo<a name="pilares"></a>
#### Cuando hablamos de la programacion orientada a objetos debemos tener en cuenta los cuatro Pilares sobre los cuales esta basada.
- El encapsulamiento
- La abstraccion 
- La herencia 
- El Polimorfismo

#### Vamos a ir viendo esos conceptos poco a poco, Iniciaremos con el pilar llamado Encapsulamiento.
# 
##  Encapsulamiento.
#### Basicamente este Pilar se refiere a la funcionalidad que esta como se nombre lo dice Encapsulada en algun objeto para que otra persona pueda utilizarla sin necesidad de conocer su comportamiento interno.
#
#### Es decir , cuando utilizamos un Carro por Ejemplo. De lo unico que tenemos que preocuparnos es de saber conducir.
#
#### Si te preguntaran cosas sobre el funcionamiento Interno del Motor , la Transmision o algun otro componente que compone este vehiculo y que es necesario para que este funcione, lo mas probable  es que no tengas idea de como estos funcionan.
#
#### Sin embargo esto no es necesario que lo sepas, ya que el automovil fue disenado para que los conductores puedan utilizarlo sin la necesidad conocer estos componentes. Para esto solo es necesario que sepas conducir para poder ir de un lado a otro con tu vehiculo.
#

#### Lo mismo paso con una funcionalidad que hemos ocupado hasta ahora, la funcionalidad seria 
~~~C#
    Console.WriteLine("Hola POO");
~~~    
#### Si te has podido dar cuenta no tenemos idea de que hace este metodo internamente porque es un metodo o una funcionalidad, pero hemos sido capaz de ocuparlo una y otra vez, ya que para eso se ha creado para imprimir un texto en la consola sin que tengamos que preocuparnos por cómo funciona este método, podemos decir que la funcionalidad de 
~~~c# 
Console.WriteLine("Hola POO"); 
~~~ 
#### está encapsulada con los conceptos anteriores en mente. vamos a proceder a crear nuestras primeras clases

#
## Que es una Clase?<a name="clases"></a>
#### Hasta ahora hemos visto acerca de las propiedades y métodos de un objeto como un automóvil o un avión, esas propiedades y métodos en el mundo de **C#** tienen que ir dentro de un concepto llamado **clase**
#### Para que quede en términos simples, una clase no es más que nada un molde. con las caracteristicas y funcionalidad que define un objeto en el mundo real ya sea tangible o intangible veamos el ejemplo.
![](https://falabella.scene7.com/is/image/FalabellaCO/3831515_1?wid=800&hei=800&qlt=70)

#### en esta Imagen tenemos una serie de moldes que especifican la forma que tendra una galleta. 
#
#### En el mundo de la construccion Algo similar sucede en esta área, los planos de casas se utilizan para llevar a cabo la construcción de una o más casas que tienen las mismas características si se siguen las especificaciones del mismo plano.
#
![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRAZkPNEcSdk6qQ7dJyS5ubdTfxNZk1RaA6HttNryXHATH1OrcvqXVN12LUfZiLKUqzqtg&usqp=CAU)

####  Lo mismo sucede en la programación orientada a objetos la clase será la plantilla que usaremos para crear varios objetos del mismo tiempo mas adelante lo veremos en detalle por el momento Quedate con la idea de que en la clase se deben especificar los metodos y atributos prueba que queremos que un objeto tenga
# 

# Ver video de ejemplo de creacion de Clases.

#
# Definiendo Metodos para la Clase 
#### ya tenemos nuestra Clase declarada con nuestras propiedades , lo siguiente es la Creacion de nuevos metodos en la misma

#### De tener dudas sobre este tema puedes consultar nuestro capitulo sobre los metodos.

#### 9 - [Metodos](#metodos)
#### En el mismo podras encontrar lo necesaria para poder crear metodos, sus tipos y caracteristicas.
# 
~~~c#
using System;
using System.Collections.Generic;
using System.Text;

namespace Rectangulo
{
    internal class Rectangulo
    {
        double baseRectangulo;
        double alturaRectangulo;
        string color;


        double CalcularArea()
        {
            // A = h * b;

            return alturaRectangulo * baseRectangulo;
        }

        double CalcularPerimetro()
        {

            // P = 2 * h + 2 * b
            return (2 * alturaRectangulo) + (2 * baseRectangulo);
        }



    }
}
~~~
#

# Creando Instancias de una Clase

#### Como puedes ver creamos dos metodos en nuestra Clase.  ***CalcularArea()*** y ***CalcularPerimetro()*** estos metodos no contienen parametros para hacer nuestros calculos debido a que los parametros que necesitamos ya estan declarados como propiedades dentro de nuestra clase.
# 
#### Bien ya hemos terminado de Definir la estructura de la clase Ahora la pregunta es cómo lo utilizamos antes de ir a ***visual Studio*** quiero que tomes especial atención a la imagen que aparece en la pantalla.
![](https://falabella.scene7.com/is/image/FalabellaCO/3831515_1?wid=800&hei=800&qlt=70)

####  Si recuerdas anteriormente hablamos sobre un ejemplo de moldes de galletas las cuales son parecidas a una clase en el hecho de que son el molde para crear objetos en el caso del molde para galletas el resultado final serán galletas podemos crear tantas galletas como queramos,  utilizando el molde y sin embargo algo que hay que tomar en cuenta es que ninguna galleta será igual.
#
#### Puede que algunas galletas salgan un poco más doradas que otras o bien que una no sea tan esponjosa como la otra.
#
####  El caso es que siempre tendremos galletas diferentes lo mismo pasa con una clase,  ***en el  caso de las clases el resultado no serán galletas sino objetos*** también conocidos Como ***instancias de una clase*** esto podría traducirse como ***objeto de una clase x*** vamos a regresar a visual estudio para crear nuestra primera instancia de una clase u objeto.


