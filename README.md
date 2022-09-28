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
