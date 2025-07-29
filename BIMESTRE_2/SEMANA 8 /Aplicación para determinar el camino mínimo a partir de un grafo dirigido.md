ALGORITMO SIN DATOS:
```java
import java.util.*;

public class KruskalSinDatos {

    static class Arista implements Comparable<Arista> {
        int origen, destino, peso;

        Arista(int origen, int destino, int peso) {
            this.origen = origen;
            this.destino = destino;
            this.peso = peso;
        }

        public int compareTo(Arista otra) {
            return this.peso - otra.peso;
        }

        @Override
        public String toString() {
            return "(" + origen + " - " + destino + ") peso: " + peso;
        }
    }

    static class Subconjunto {
        int padre, rango;
    }

    static int encontrar(Subconjunto[] subconjuntos, int i) {
        if (subconjuntos[i].padre != i)
            subconjuntos[i].padre = encontrar(subconjuntos, subconjuntos[i].padre);
        return subconjuntos[i].padre;
    }

    static void unir(Subconjunto[] subconjuntos, int x, int y) {
        int xroot = encontrar(subconjuntos, x);
        int yroot = encontrar(subconjuntos, y);

        if (subconjuntos[xroot].rango < subconjuntos[yroot].rango)
            subconjuntos[xroot].padre = yroot;
        else if (subconjuntos[xroot].rango > subconjuntos[yroot].rango)
            subconjuntos[yroot].padre = xroot;
        else {
            subconjuntos[yroot].padre = xroot;
            subconjuntos[xroot].rango++;
        }
    }

    public static void main(String[] args) {
        // Datos directos (nodos pueden ser cualquier entero)
        int[][] datos = {
                {1, 2, 3},
                {1, 5, 6},
                {5, 2, 10}
        };

        // Mapear nodos reales a índices internos
        Set<Integer> nodos = new HashSet<>();
        for (int[] d : datos) {
            nodos.add(d[0]);
            nodos.add(d[1]);
        }

        // Crear mapa de nodo real -> índice
        Map<Integer, Integer> mapaNodos = new HashMap<>();
        int idx = 0;
        for (int nodo : nodos) {
            mapaNodos.put(nodo, idx++);
        }

        int V = nodos.size();
        List<Arista> aristas = new ArrayList<>();

        for (int[] d : datos) {
            int origenIdx = mapaNodos.get(d[0]);
            int destinoIdx = mapaNodos.get(d[1]);
            aristas.add(new Arista(origenIdx, destinoIdx, d[2]));
        }

        kruskal(V, aristas, mapaNodos);
    }

    public static void kruskal(int V, List<Arista> aristas, Map<Integer, Integer> mapaInverso) {
        List<Arista> resultado = new ArrayList<>();

        Collections.sort(aristas);
        System.out.println("Aristas ordenadas por peso:");
        for (Arista a : aristas)
            System.out.println("  " + a);

        Subconjunto[] subconjuntos = new Subconjunto[V];
        for (int i = 0; i < V; ++i) {
            subconjuntos[i] = new Subconjunto();
            subconjuntos[i].padre = i;
            subconjuntos[i].rango = 0;
        }

        System.out.println("\nSeleccionando aristas para el MST:");

        for (Arista arista : aristas) {
            int x = encontrar(subconjuntos, arista.origen);
            int y = encontrar(subconjuntos, arista.destino);

            if (x != y) {
                resultado.add(arista);
                unir(subconjuntos, x, y);
                System.out.println(" Arista añadida: " + arista);
            } else {
                System.out.println("Arista descartada (crea ciclo): " + arista);
            }

            if (resultado.size() == V - 1)
                break;
        }

        System.out.println("\nÁrbol de recubrimiento mínimo resultante:");
        int pesoTotal = 0;
        for (Arista a : resultado) {
            System.out.println(a);
            pesoTotal += a.peso;
        }

        System.out.println("Peso total del Árbol de Recubrimiento Mínimo: " + pesoTotal);
    }
}


```


SALIDA:
<img width="1919" height="1013" alt="image" src="https://github.com/user-attachments/assets/3380f24d-31a4-4f29-b5e2-0a02739ca995" />





ALGORITMO INGRESANDO DATOS:

```java
import java.util.*;

public class Kruskal {

    // Estructura para representar una arista
    static class Arista implements Comparable<Arista> {
        int origen, destino, peso;

        Arista(int origen, int destino, int peso) {
            this.origen = origen;
            this.destino = destino;
            this.peso = peso;
        }

        public int compareTo(Arista otra) {
            return this.peso - otra.peso;
        }

        @Override
        public String toString() {
            return "(" + origen + " - " + destino + ") peso: " + peso;
        }
    }


    static class Subconjunto {
        int padre, rango;
    }

    static int encontrar(Subconjunto[] subconjuntos, int i) {
        if (subconjuntos[i].padre != i)
            subconjuntos[i].padre = encontrar(subconjuntos, subconjuntos[i].padre);
        return subconjuntos[i].padre;
    }

    static void unir(Subconjunto[] subconjuntos, int x, int y) {
        int xroot = encontrar(subconjuntos, x);
        int yroot = encontrar(subconjuntos, y);

        if (subconjuntos[xroot].rango < subconjuntos[yroot].rango)
            subconjuntos[xroot].padre = yroot;
        else if (subconjuntos[xroot].rango > subconjuntos[yroot].rango)
            subconjuntos[yroot].padre = xroot;
        else {
            subconjuntos[yroot].padre = xroot;
            subconjuntos[xroot].rango++;
        }
    }

    public static void kruskal(int V, List<Arista> aristas) {
        List<Arista> resultado = new ArrayList<>();

        // Ordenar las aristas por peso
        Collections.sort(aristas);
        System.out.println("Aristas ordenadas por peso:");
        for (Arista a : aristas)
            System.out.println("  " + a);

        // Crear subconjuntos
        Subconjunto[] subconjuntos = new Subconjunto[V];
        for (int i = 0; i < V; ++i) {
            subconjuntos[i] = new Subconjunto();
            subconjuntos[i].padre = i;
            subconjuntos[i].rango = 0;
        }

        System.out.println("\nSeleccionando aristas para el MST:");

        for (Arista arista : aristas) {
            int x = encontrar(subconjuntos, arista.origen);
            int y = encontrar(subconjuntos, arista.destino);

            if (x != y) {
                resultado.add(arista);
                unir(subconjuntos, x, y);
                System.out.println(" Arista añadida: " + arista);
            } else {
                System.out.println("Arista descartada (crea ciclo): " + arista);
            }

            if (resultado.size() == V - 1)
                break;
        }

        System.out.println("\nÁrbol de recubrimiento mínimo resultante:");
        int pesoTotal = 0;
        for (Arista a : resultado) {
            System.out.println(a);
            pesoTotal += a.peso;
        }

        System.out.println("Peso total del Árbol de Recubrimiento Mínimo: " + pesoTotal);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el número de vértices: ");
        int V = scanner.nextInt();

        System.out.print("Ingrese el número de aristas: ");
        int E = scanner.nextInt();

        List<Arista> aristas = new ArrayList<>();

        System.out.println("Ingrese cada arista (formato: origen destino peso):");
        for (int i = 0; i < E; i++) {
            int origen = scanner.nextInt();
            int destino = scanner.nextInt();
            int peso = scanner.nextInt();
            aristas.add(new Arista(origen, destino, peso));
        }

        kruskal(V, aristas);

        scanner.close();
    }
}


```

SALIDA:
<img width="1916" height="1011" alt="image" src="https://github.com/user-attachments/assets/983c8f91-c6fa-4f8d-837e-81cefdcbdcf2" />


