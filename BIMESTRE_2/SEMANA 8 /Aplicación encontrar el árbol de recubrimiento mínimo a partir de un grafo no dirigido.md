CODIGO SIN DATOS :
import java.util.*;

public class DijkstraAppSINDATOS {
    static final int INF = Integer.MAX_VALUE;

    static class Grafo {
        int vertices;
        int[][] matrizAdyacencia;

        public Grafo(int v) {
            this.vertices = v;
            matrizAdyacencia = new int[v][v];


            for (int i = 0; i < v; i++) {
                Arrays.fill(matrizAdyacencia[i], INF);
                matrizAdyacencia[i][i] = 0;
            }
        }

        public void agregarArista(int origen, int destino, int peso) {
            matrizAdyacencia[origen][destino] = peso;
        }

        public void dijkstra(int inicio) {
            int[] dist = new int[vertices];
            boolean[] visitado = new boolean[vertices];

            Arrays.fill(dist, INF);
            dist[inicio] = 0;

            for (int i = 0; i < vertices - 1; i++) {
                int u = obtenerMinimo(dist, visitado);
                visitado[u] = true;

                for (int v = 0; v < vertices; v++) {
                    if (!visitado[v] && matrizAdyacencia[u][v] != INF &&
                            dist[u] != INF && dist[u] + matrizAdyacencia[u][v] < dist[v]) {
                        dist[v] = dist[u] + matrizAdyacencia[u][v];
                    }
                }
            }

            mostrarResultado(dist, inicio);
        }

        private int obtenerMinimo(int[] dist, boolean[] visitado) {
            int min = INF, minIndex = -1;

            for (int v = 0; v < vertices; v++) {
                if (!visitado[v] && dist[v] <= min) {
                    min = dist[v];
                    minIndex = v;
                }
            }
            return minIndex;
        }

        private void mostrarResultado(int[] dist, int inicio) {
            System.out.println("Distancias mínimas desde el nodo " + inicio + ":");
            for (int i = 0; i < vertices; i++) {
                System.out.println("A nodo " + i + " => " + (dist[i] == INF ? "∞" : dist[i]));
            }
        }
    }

    public static void main(String[] args) {

        Grafo grafo = new Grafo(5);


        grafo.agregarArista(0, 1, 10);
        grafo.agregarArista(0, 4, 5);
        grafo.agregarArista(1, 2, 1);
        grafo.agregarArista(1, 4, 2);
        grafo.agregarArista(2, 3, 4);
        grafo.agregarArista(3, 0, 7);
        grafo.agregarArista(4, 1, 3);
        grafo.agregarArista(4, 2, 9);
        grafo.agregarArista(4, 3, 2);


        grafo.dijkstra(0);
    }
}


SALIDA:

<img width="1919" height="1010" alt="image" src="https://github.com/user-attachments/assets/babdad5b-4263-43e6-b483-b87b452d4f51" />

CODIGO INGRESANDO DATOS:
import java.util.*;

public class DijkstraApp {
    static final int INF = Integer.MAX_VALUE;

    static class Grafo {
        int vertices;
        int[][] matrizAdyacencia;

        public Grafo(int v) {
            this.vertices = v;
            matrizAdyacencia = new int[v][v];

            for (int i = 0; i < v; i++) {
                Arrays.fill(matrizAdyacencia[i], INF);
                matrizAdyacencia[i][i] = 0;
            }
        }

        public void agregarArista(int origen, int destino, int peso) {
            matrizAdyacencia[origen][destino] = peso;
        }

        public void dijkstra(int inicio) {
            int[] dist = new int[vertices];
            boolean[] visitado = new boolean[vertices];

            Arrays.fill(dist, INF);
            dist[inicio] = 0;

            for (int i = 0; i < vertices - 1; i++) {
                int u = obtenerMinimo(dist, visitado);
                visitado[u] = true;

                for (int v = 0; v < vertices; v++) {
                    if (!visitado[v] && matrizAdyacencia[u][v] != INF &&
                            dist[u] != INF && dist[u] + matrizAdyacencia[u][v] < dist[v]) {
                        dist[v] = dist[u] + matrizAdyacencia[u][v];
                    }
                }
            }

            mostrarResultado(dist, inicio);
        }

        private int obtenerMinimo(int[] dist, boolean[] visitado) {
            int min = INF, minIndex = -1;

            for (int v = 0; v < vertices; v++) {
                if (!visitado[v] && dist[v] <= min) {
                    min = dist[v];
                    minIndex = v;
                }
            }
            return minIndex;
        }

        private void mostrarResultado(int[] dist, int inicio) {
            System.out.println("Distancias mínimas desde el nodo " + inicio + ":");
            for (int i = 0; i < vertices; i++) {
                System.out.println("A nodo " + i + " => " + (dist[i] == INF ? "∞" : dist[i]));
            }
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Ingrese número de vértices: ");
        int v = sc.nextInt();
        Grafo grafo = new Grafo(v);

        System.out.print("Ingrese número de aristas: ");
        int e = sc.nextInt();

        System.out.println("Ingrese cada arista en el formato: origen destino peso");
        for (int i = 0; i < e; i++) {
            int origen = sc.nextInt();
            int destino = sc.nextInt();
            int peso = sc.nextInt();
            grafo.agregarArista(origen, destino, peso);
        }

        System.out.print("Ingrese el nodo inicial: ");
        int inicio = sc.nextInt();

        grafo.dijkstra(inicio);
    }
}

SALIDA:
<img width="1919" height="1020" alt="image" src="https://github.com/user-attachments/assets/12dee6a9-c9fa-4e43-b338-41de9db7e369" />

