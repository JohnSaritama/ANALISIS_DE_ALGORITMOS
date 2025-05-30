# Sucesión de Fibonacci

## 1. Algoritmo en Java

### Versión Recursiva

```java
public class FibonacciRecursivo {
    public static int fibonacci(int n) {
        if (n <= 1) return n;
        return fibonacci(n - 1) + fibonacci(n - 2);
    }

    public static void main(String[] args) {
        int n = 10;
        System.out.println("Fibonacci(" + n + ") = " + fibonacci(n));
    }
}
```

### Versión Iterativa

```java
public class FibonacciIterativo {
    public static int fibonacci(int n) {
        if (n <= 1) return n;
        int a = 0, b = 1, c;
        for (int i = 2; i <= n; i++) {
            c = a + b;
            a = b;
            b = c;
        }
        return b;
    }

    public static void main(String[] args) {
        int n = 10;
        System.out.println("Fibonacci(" + n + ") = " + fibonacci(n));
    }
}
```

---

## 2. Identificación de la Recurrencia

La sucesión de Fibonacci se define como:

- F(0) = 0  
- F(1) = 1  
- F(n) = F(n-1) + F(n-2), para n ≥ 2

Esta es una **relación de recurrencia lineal homogénea de segundo orden con coeficientes constantes**.

---

## 3. Ecuación General (Fórmula Cerrada de Binet)

### Paso 1: Suposición de solución

Asumimos que F(n) = rⁿ. Reemplazamos en la recurrencia:

```
rⁿ = rⁿ⁻¹ + rⁿ⁻²  
Dividiendo entre rⁿ⁻²:  
r² = r + 1  
```

### Paso 2: Resolver la ecuación característica

```
r² - r - 1 = 0  
```

Soluciones:

```
φ = (1 + √5) / 2  
ψ = (1 - √5) / 2
```

### Paso 3: Forma general de la solución

```
F(n) = A * φⁿ + B * ψⁿ
```

Usando las condiciones iniciales:

- F(0) = 0 → A + B = 0 → B = -A  
- F(1) = 1 → A(φ - ψ) = 1 → A = 1/√5

Entonces:

```
F(n) = (1 / √5) * (φⁿ - ψⁿ)
```

### Fórmula final:

```
F(n) = (1 / √5) * [ ((1 + √5)/2)^n - ((1 - √5)/2)^n ]
```

---

## 4. Demostración por Inducción

### Base:

- F(0) = (1/√5)(1 - 1) = 0  
- F(1) = (1/√5)(φ - ψ) = 1

### Paso inductivo:

Suponemos:

- F(k) = (1/√5)(φ^k - ψ^k)  
- F(k-1) = (1/√5)(φ^(k-1) - ψ^(k-1))

Entonces:

```
F(k+1) = F(k) + F(k-1)  
       = (1/√5)(φ^k + φ^(k-1) - ψ^k - ψ^(k-1))  
       = (1/√5)(φ^(k+1) - ψ^(k+1))
```

Demostrado.
