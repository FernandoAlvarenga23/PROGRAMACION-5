# PROGRAMACION-5
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            operaciones tt = new operaciones();
            tt.metodomenu();  
          
        }
    }
}


class operaciones
{
    public int op = 0; 
    public double v1 = 0, v2 = 0;
   

    public void metodomenu()
    {

        do
        {
            Console.Clear();

            Console.WriteLine("Digite el numero de la operacion a realizar");
            Console.WriteLine("1.Area de un Triangulo");
            Console.WriteLine("2.Area de un Rectangulo ");
            Console.WriteLine("3.Area de un Circulo");
            op = int.Parse(Console.ReadLine());

        } while (op != 1 && op != 2 && op != 3);//mientras que no digite una de las opciones en el menu se repetira

        if (op == 1) { uno(); }
        if (op == 2) { dos(); }
        if (op == 3) { tres(); }

    }


    public void uno()
    {

        Console.Clear();
        Console.WriteLine("Area de un Triangulo");
        Console.WriteLine("Digite la base");
        v1 = double.Parse(Console.ReadLine());
        Console.WriteLine("Digite la altura");
        v2 = double.Parse(Console.ReadLine());
        double v3 = (v1*v2)/2;

        Console.WriteLine("Area del Triangulo: " + v3 + "cm^2");
        continuar();

    }




    public void dos()
    {

        Console.Clear();
        Console.WriteLine("Area de un Rectangulo");
        Console.WriteLine("Digite la base");
        v1 = double.Parse(Console.ReadLine());
        Console.WriteLine("Digite la altura");
        v2 = double.Parse(Console.ReadLine());
        double v4 = v2 * v1;//area
    
        Console.WriteLine("Area del Rectangulo: " + v4 + "cm^2");
        continuar();

    }

    public void tres()
    {
        Console.Clear();
        Console.WriteLine("Area de un Circulo");
        Console.WriteLine("Digite radio del circulo");
        v1 = double.Parse(Console.ReadLine());
        double v4 = 3.1416 * (Math.Pow(v1, 2));//area
        Console.WriteLine("Area del Ciruclo: " + v4 + "cm^2");
        continuar();
    }



    public void continuar()
    {
         char l = 'a';

        while (l == 'a' )
        {
        Console.WriteLine("\n\n");
        Console.WriteLine("Desea Continuar s=si, n=no");
        l =Convert.ToChar (Console.ReadLine());


        if (l == 's' || l == 'S') { metodomenu(); }//regresamos al menu
        if (l == 'n' || l == 'N')
        {//si digitamos n o N un mensaje de despedida 
            Console.WriteLine("Adios");
            l = 'b';
            Console.ReadKey(true);
        }
        else
        {
            l = 'a';
            Console.Clear();
        }//cierre else

        }

       
        
    }

}
