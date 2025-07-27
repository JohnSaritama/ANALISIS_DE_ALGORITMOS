# Taller: Generación de números Pseudoaleatorios

## OPCIÓN 1:
```java
public class GeneradorPseudoaleatorio {

    public static void main(String[] args) {
        int cantidad = 10;
        long semilla = 12345;
        int rango_max = 50;

        int[] numeros = generarPseudoaleatorios(semilla, cantidad, rango_max);

        System.out.println("Números pseudoaleatorios generados:");
        for (int num : numeros) {
            System.out.println(num);
        }
    }

    public static int[] generarPseudoaleatorios(long semilla, int cantidad, int rango_max) {
        // Parámetros del generador
        long a = 1664525;
        long c = 1013904223;
        long m = (long) Math.pow(2, 32);

        int[] resultados = new int[cantidad];
        long x = semilla;

        for (int i = 0; i < cantidad; i++) {
            x = (a * x + c) % m;
            resultados[i] = (int)(x % (rango_max + 1)); 
        }

        return resultados;
    }
}
```
SALIDA:

<img width="1919" height="1015" alt="image" src="https://github.com/user-attachments/assets/b619126c-f326-45e9-95b0-cd3440e125d4" />


## OPCIÓN 2:

```java
import java.util.Scanner;

public class GeneradorPseudoaleatorioINGRESANDO_DATOS {



        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);

            System.out.println("=== Generador de Números Pseudoaleatorios ===");

            System.out.print("Ingrese la cantidad de números a generar: ");
            int cantidad = scanner.nextInt();

            System.out.print("Ingrese la semilla inicial (entero positivo): ");
            long semilla = scanner.nextLong();

            System.out.print("Ingrese el valor máximo del rango (mínimo es 0): ");
            int rango_max = scanner.nextInt();

            int[] numeros = generarPseudoaleatorios(semilla, cantidad, rango_max);

            System.out.println("\nNúmeros pseudoaleatorios generados:");
            for (int num : numeros) {
               System.out.print(" "+num+"|");
            }

            scanner.close();
        }

        public static int[] generarPseudoaleatorios(long semilla, int cantidad, int rango_max) {
            long a = 1664525;
            long c = 1013904223;
            long m = (long) Math.pow(2, 32);

            int[] resultados = new int[cantidad];
            long x = semilla;

            for (int i = 0; i < cantidad; i++) {
                x = (a * x + c) % m;
                resultados[i] = (int)(x % (rango_max + 1));
            }

            return resultados;
        }
    }


```

SALIDA:

<img width="1910" height="1000" alt="image" src="https://github.com/user-attachments/assets/cfe59622-5d04-4712-baf3-94a0b62028a1" />

