/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */
package practica3;

import java.util.Scanner;

/**
 *
 * @author user
 */
public class Practica3 {

    /**
     * @param args the command line arguments
     */
      public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
 int categoria, i, n, ventas_entre_500_y_1000, ventas_mayores_a_1000;
        int ventas_menores_a_500;
        double monto_de_jugueteria, monto_de_deportes, monto_de_caballeros, monto_de_jardineria, monto_de_damas;
        double monto_de_lacteos, monto_de_panaderia, monto_global, venta;
        ventas_entre_500_y_1000 = 0;
        ventas_mayores_a_1000 = 0;
        ventas_menores_a_500 = 0;
        monto_de_jugueteria = 0;
        monto_de_deportes = 0;
        monto_de_caballeros = 0;
        monto_de_jardineria = 0;
        monto_de_damas = 0;
        monto_de_lacteos = 0;
        monto_de_panaderia = 0;
        monto_global = 0;
        System.out.print("Ingresa el valor de n: ");
        n = in.nextInt();
        in.nextLine();
        for (i=1; i<=n; i++) {
            System.out.print("Proceso # " + i);
            System.out.print(" : Ingresa el valor de venta: ");
            venta = in.nextDouble();
            in.nextLine();
            System.out.println("Selecciona la categoria del valor anterior.");
            System.out.println("\t1.- jugueteria");
            System.out.println("\t2.- deportes");
            System.out.println("\t3.- caballeros");
            System.out.println("\t4.- damas");
            System.out.println("\t5.- lacteos");
            System.out.println("\t6.- jardineria");
            System.out.println("\t7.- panaderia");
            System.out.print("\t: ");
            do {
                categoria = in.nextInt();
                in.nextLine();
                if (categoria<1||categoria>7)
                    System.out.print("Valor incorrecto. Ingresalo nuevamente.: ");
            } while (categoria<1||categoria>7);
            if(venta>1000)
                ventas_mayores_a_1000=ventas_mayores_a_1000+1;
            if(venta>500&&venta<=1000)
                ventas_entre_500_y_1000=ventas_entre_500_y_1000+1;
            if(venta<=500)
                ventas_menores_a_500=ventas_menores_a_500+1;
            monto_global=monto_global+venta;
            if(categoria==1)
                monto_de_jugueteria=monto_de_jugueteria+venta;
            if(categoria==2)
                monto_de_deportes=monto_de_deportes+venta;
            if(categoria==3)
                monto_de_caballeros=monto_de_caballeros+venta;
            if(categoria==4)
                monto_de_damas=monto_de_damas+venta;
            if(categoria==5)
                monto_de_lacteos=monto_de_lacteos+venta;
            if(categoria==6)
                monto_de_jardineria=monto_de_jardineria+venta;
            if(categoria==7)
                monto_de_panaderia=monto_de_panaderia+venta;
            System.out.println();
        }
        System.out.println("Valor de ventas entre 500 y 1000: " + ventas_entre_500_y_1000);
        System.out.println("Valor de ventas mayores a 1000: " + ventas_mayores_a_1000);
        System.out.println("Valor de ventas menores a 500: " + ventas_menores_a_500);
        System.out.println("Valor de monto de jugueteria: " + monto_de_jugueteria);
        System.out.println("Valor de monto de deportes: " + monto_de_deportes);
        System.out.println("Valor de monto de caballeros: " + monto_de_caballeros);
        System.out.println("Valor de monto de jardineria: " + monto_de_jardineria);
        System.out.println("Valor de monto de damas: " + monto_de_damas);
        System.out.println("Valor de monto de lacteos: " + monto_de_lacteos);
        System.out.println("Valor de monto de panaderia: " + monto_de_panaderia);
        System.out.println("Valor de monto global: " + monto_global);
    }

}
