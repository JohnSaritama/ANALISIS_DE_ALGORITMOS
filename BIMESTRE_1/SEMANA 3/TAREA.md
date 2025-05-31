  CODIGO EN JAVA:
```java


public class MergeSortHelper {
    public static void merge(int[] A, int p, int q, int r) {
        int nL = q - p + 1; // length of A[p..q]
        int nR = r - q;     // length of A[q+1..r]

        // Create temporary arrays
        int[] L = new int[nL];
        int[] R = new int[nR];

        // Copy A[p..q] into L[0..nL-1]
        for (int i = 0; i < nL; i++) {
            L[i] = A[p + i];
        }

        // Copy A[q+1..r] into R[0..nR-1]
        for (int j = 0; j < nR; j++) {
            R[j] = A[q + 1 + j];
        }

        int i = 0; // index for L
        int j = 0; // index for R
        int k = p; // index for A

        // Merge L and R into A[p..r]
        while (i < nL && j < nR) {
            if (L[i] <= R[j]) {
                A[k] = L[i];
                i++;
            } else {
                A[k] = R[j];
                j++;
            }
            k++;
        }

        // Copy any remaining elements of L
        while (i < nL) {
            A[k] = L[i];
            i++;
            k++;
        }

        // Copy any remaining elements of R
        while (j < nR) {
            A[k] = R[j];
            j++;
            k++;
        }
    }
}

```

PARA METER NUMEROS DE CONSOLA: 
```java
import java.util.Scanner;

public class MergeSortHelper {

  
    public static void merge(int[] A, int p, int q, int r) {
        int nL = q - p + 1;
        int nR = r - q;

        int[] L = new int[nL];
        int[] R = new int[nR];

        for (int i = 0; i < nL; i++) {
            L[i] = A[p + i];
        }

        for (int j = 0; j < nR; j++) {
            R[j] = A[q + 1 + j];
        }

        int i = 0, j = 0, k = p;

        while (i < nL && j < nR) {
            if (L[i] <= R[j]) {
                A[k++] = L[i++];
            } else {
                A[k++] = R[j++];
            }
        }

        while (i < nL) {
            A[k++] = L[i++];
        }

        while (j < nR) {
            A[k++] = R[j++];
        }
    }



    // Función principal para ingresar los numeros del arreglo
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese la cantidad de elementos: ");
        int n = scanner.nextInt();
        int[] A = new int[n];

        System.out.println("Ingrese los elementos del arreglo:");
        for (int i = 0; i < n; i++) {
            A[i] = scanner.nextInt();
        }

       

        System.out.println("Arreglo ordenado:");
        for (int i = 0; i < n; i++) {
            System.out.print(A[i] + " ");
        }

        scanner.close();
    }
}
```


### Prueba de escritorio

#### Datos de entrada:
- A = {2, 5, 8, 1, 3, 7}
- p = 0, q = 2, r = 5

#### Variables derivadas:
- L = {2, 5, 8}
- R = {1, 3, 7}

#### Prueba de escritorio:

| i | j | k | L[i] | R[j] | A[k] antes | A[k] después | Comentario                        |
|---|---|---|------|------|-------------|---------------|-----------------------------------|
| 0 | 0 | 0 | 2    | 1    | 2           | 1             | R[j] < L[i], copiar R[j] en A[k]  |
| 0 | 1 | 1 | 2    | 3    | 5           | 2             | L[i] < R[j], copiar L[i] en A[k]  |
| 1 | 1 | 2 | 5    | 3    | 8           | 3             | R[j] < L[i], copiar R[j] en A[k]  |
| 1 | 2 | 3 | 5    | 7    | 1           | 5             | L[i] < R[j], copiar L[i] en A[k]  |
| 2 | 2 | 4 | 8    | 7    | 3           | 7             | R[j] < L[i], copiar R[j] en A[k]  |
| 2 | 3 | 5 | 8    | -    | 7           | 8             | Copiar el resto de L a A          |

#### Resultado final:
- A = {1, 2, 3, 5, 7, 8}

### Conclusión

Este paso de fusión implementa de manera eficiente la combinación de dos subarreglos ordenados en un solo arreglo ordenado, utilizando el paradigma de divide y venceras.
