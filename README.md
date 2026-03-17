using System; 

  

class Program 

{ 

    static void Main() 

    { 

        int n; 

  

        Console.Write("¿Cuántos números deseas ingresar?: "); 

        string? line = Console.ReadLine(); 

        while (!int.TryParse(line, out n) || n < 0) 

        { 

            Console.Write("Entrada inválida. Ingrese un número entero no negativo: "); 

            line = Console.ReadLine(); 

        } 

  

        int pares = 0; 

        int impares = 0; 

        int mayores10 = 0; 

        int positivos = 0; 

        int negativos = 0; 

  

        for (int i = 0; i < n; i++) 

        { 

            Console.Write("Ingrese un número: "); 

            string? input = Console.ReadLine(); 

            int num; 

            while (!int.TryParse(input, out num)) 

            { 

                Console.Write("Entrada inválida. Ingrese un número entero: "); 

                input = Console.ReadLine(); 

            } 

  

            // Pares e impares 

            if (num % 2 == 0) 

                pares++; 

            else 

                impares++; 

  

            // Mayores a 10 

            if (num > 10) 

                mayores10++; 

  

            // Positivos y negativos 

            if (num > 0) 

                positivos++; 

            else if (num < 0) 

                negativos++; 

        } 

  

        Console.WriteLine("\nResultados:"); 

        Console.WriteLine("Cantidad de pares: " + pares); 

        Console.WriteLine("Cantidad de impares: " + impares); 

        Console.WriteLine("Cantidad mayores a 10: " + mayores10); 

        Console.WriteLine("Cantidad de positivos: " + positivos); 

        Console.WriteLine("Cantidad de negativos: " + negativos); 

    } 

} 
