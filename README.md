
## Repositorio de Problemas y Programas de Métodos Numéricos


¡Bienvenido al repositorio de Métodos Numéricos Tema 4 - Integración Numérica!

Este repositorio está diseñado para proporcionarte acceso a una variedad de algoritmos, programas y pruebas de ejecución que se centran en los siguientes métodos de integración numérica:

Método del Trapecio: Un enfoque fundamental que aproxima el área bajo una curva dividiéndola en trapezoides y sumando las áreas de estos trapezoides, ofreciendo una solución simple pero efectiva para calcular integrales definidas.

Método de Simpson 1/3: Un método más preciso que el Método del Trapecio, que utiliza polinomios de segundo orden (parábolas) para estimar el área bajo la curva, proporcionando una aproximación más precisa de la integral definida.

Método de Simpson 3/8: Una extensión del Método de Simpson 1/3 que utiliza polinomios de tercer orden (cúbicos) para aproximar la función y ofrecer una mayor precisión en la estimación del área bajo la curva.

En este repositorio, no solo encontrarás la descripción teórica de cada método, sino también implementaciones prácticas en forma de programas y algoritmos. Además, se proporcionan pruebas de ejecución detalladas que te guiarán a través del proceso de aplicación de cada método, brindándote una comprensión profunda y práctica de su funcionamiento en el contexto de la integración numérica.
## Contenido del Repositorio

## Método del Trapecio

- [Descripción](#descripción-método-trapecio)
- [Algoritmo](#algoritmo-de-trapecio)
- [Ejemplos](#ejemplos-trapecio)
- [Implementación](#implementacion-método-trapecio)


## Método Simpson 1/3

- [Descripción](#descripción-simpson-1/3)
- [Algoritmo](#algoritmo-simpson-1/3)
- [Ejemplos](#ejemplos-simpson-1/3)
- [Implementación](#implementación-simpson-1/3)

## Método Eliminación Gaussiana

- [Descripción](#descripción-eliminación-gaussiana)
- [Algoritmo](#algoritmo-eliminación-gaussiana)
- [Ejemplos](#ejemplos-eliminación-gaussiana)
-  [Implementación](#implementación-eliminación-gaussiana)

---

## Método de Trapecio

### Descripción Método Trapecio

El método del trapecio es uno de los métodos de integración numérica más simples pero efectivos. Divide el área bajo la curva en múltiples trapecios y calcula la suma de las áreas de estos trapecios para estimar la integral. La fórmula básica para el método del trapecio se basa en la aproximación de que la función es lineal entre los puntos de la partición.

![image](https://github.com/xlmdn/problemarioT4/assets/147437527/a35f18f1-4a9b-47c0-b146-2722b72fd2ec)


### Algoritmo De Trapecio

![image](https://github.com/xlmdn/problemarioT4/assets/147437527/94107b98-c072-411a-adc6-cd63e6c2f817)


## Implementacion Método Trapecio

public class trapecio {
    public static void main(String[] args) {
        //funcion 2x+ 10 en a=1 b=3
        int a,b,fa,fb,res;
        a=1;
        b=3;
        fa =2*a+10;
        fb=2*b+10;
        res=(b-a)*((fa+fb)/2);
        System.out.println("El area del trapecio es: "+res);
    }
}

## Ejemplos Trapecio

## Ejemplo 1



## Ejemplo 2



## Ejemplo 3


## Ejemplo 4



## Ejemplo 5







## Método Simpson 1/3

### Descripción Simpson 1/3

El método de Simpson 1/3 es un método más preciso que el método del trapecio y utiliza polinomios de segundo orden (parábolas) para estimar el área bajo la curva. Divide el intervalo de integración en segmentos de igual longitud y aplica la fórmula de Simpson 1/3 en cada par de segmentos adyacentes.

![image](https://github.com/xlmdn/problemarioT4/assets/147437527/2bc0b915-aacc-47ea-8a9b-3d98dad70ffc)



### Algoritmo Simpson 1/3

![image](https://github.com/xlmdn/problemarioT4/assets/147437527/a7b9a805-7cc9-4c9c-a6ec-d749085a0d35)


## Implementación Simpson 1/3

public static void main(String[] args) {
        // función 2x^2 + 10 en a=1, b=3
        int a, b, fa, fb;
        double fq, fqq,res;
        a = 1;
        b = 3;
        fa = 2 *(a*a) + 10;
        fb = 2 * (b*b) + 10;
        fq = (a + b) / 2.0; // Usar double para evitar truncamiento
        fqq = 2 * (fq*fq) + 10;
        res = (int) ((b - a) / 6.0 * (fa + 4 * fqq + fb)); // Convertir a int al final
        System.out.println("El área bajo la curva es: " + res);
    }


### Ejemplos Simpson 1/3

## Ejemplo 1



## Método Eliminación Gaussiana

### Descripción Eliminación Gaussiana

La eliminación gaussiana es un método utilizado para resolver sistemas de ecuaciones lineales mediante la transformación de la matriz aumentada del sistema en una forma escalonada mediante operaciones elementales de fila. Este método es fundamental en álgebra lineal y es utilizado en numerosos campos de la ciencia y la ingeniería.

![image](https://github.com/xlmdn/problemario/assets/147437527/81b465d1-d655-465b-862a-d56b6e940917)


### Algoritmo Eliminación Gaussiana

-Inicialización: Comenzamos con una matriz aumentada que representa el sistema de ecuaciones lineales.

-Iteración por filas: Recorremos la matriz por filas de arriba hacia abajo y aplicamos las siguientes operaciones para cada fila:

Pivoteo parcial (opcional): Si es necesario, intercambiamos filas para asegurar que el elemento en la posición de pivote (el primer elemento no nulo de la fila actual) sea el mayor en magnitud entre todos los elementos de la columna.

Escalonamiento: Convertimos todos los elementos debajo del pivote en ceros, utilizando operaciones de fila. Para cada fila por debajo de la fila actual, restamos un múltiplo apropiado de la fila actual de manera que el elemento correspondiente se vuelva cero.

-Verificación de solución única: Después de llevar la matriz a su forma escalonada, verificamos si el sistema tiene una única solución, ninguna solución o infinitas soluciones. Esto puede hacerse verificando si hay alguna fila completamente nula o si hay una fila con ceros en todas las columnas excepto en la última.

-Sustitución hacia atrás (si es necesario): Si el sistema tiene una solución única, realizamos la sustitución hacia atrás para encontrar los valores de las incógnitas.

# Implementación Eliminación Gaussiana



    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Pedir al usuario las dimensiones de la matriz
        System.out.println("Ingrese el número de filas de la matriz:");
        int filas = scanner.nextInt();
        System.out.println("Ingrese el número de columnas de la matriz:");
        int columnas = scanner.nextInt();

        // Declarar las matrices y el vector
        double[][] A = new double[filas][columnas];
        double[][] B = new double[filas][1];

        // Pedir al usuario los valores de la matriz A
        System.out.println("Ingrese los elementos de la matriz A:");
        for (int i = 0; i < filas; i++) {
            for (int j = 0; j < columnas; j++) {
                System.out.print("A[" + i + "][" + j + "]: ");
                A[i][j] = scanner.nextDouble();
            }
        }

        // Pedir al usuario los valores del vector B
        System.out.println("Ingrese los elementos del vector B:");
        for (int i = 0; i < filas; i++) {
            System.out.print("B[" + i + "]: ");
            B[i][0] = scanner.nextDouble();
        }

        // Realizar el algoritmo de eliminación de Gauss
        // Copiamos las matrices originales y las hacemos de tipo flotante
        double[][] A_copy = new double[A.length][A[0].length];
        double[][] B_copy = new double[B.length][B[0].length];

        for (int i = 0; i < A.length; i++) {
            A_copy[i] = Arrays.copyOf(A[i], A[i].length);
            B_copy[i] = Arrays.copyOf(B[i], B[i].length);
        }

        // Se calcula el tamaño del vector
        int N = B.length;

        // Se recorre la matriz
        for (int i = 0; i < N; i++) {
            // Normalización
            double pivot = A_copy[i][i];
            System.out.println("Mi pivote es: " + pivot);
            for (int j = 0; j < A_copy[i].length; j++) {
                A_copy[i][j] /= pivot;
            }
            B_copy[i][0] /= pivot;
            System.out.println("\nSe divide el renglon por el pivote:");
            printMatrix(A_copy);
            System.out.println("\nSe divide el vector por el pivote:");
            printMatrix(B_copy);

            // Eliminación hacia adelante
            for (int j = i + 1; j < N; j++) {
                double factor = A_copy[j][i];
                System.out.println("\nConvertir en cero la matriz");
                System.out.println(factor);
                for (int k = 0; k < A_copy[j].length; k++) {
                    A_copy[j][k] -= factor * A_copy[i][k];
                }
                B_copy[j][0] -= factor * B_copy[i][0];
                printMatrix(A_copy);
                printMatrix(B_copy);
            }
        }

        // Sustitución hacia atrás
        double[] x = new double[N];
        for (int i = N - 1; i >= 0; i--) {
            System.out.println("\nIteracion " + i);
            System.out.println("B_copy[" + i + "]: " + B_copy[i][0]);
            System.out.println("A_copy[" + i + ", " + (i + 1) + ":]: " + Arrays.toString(Arrays.copyOfRange(A_copy[i], i + 1, A_copy[i].length)));
            System.out.println("x[" + (i + 1) + ":]: " + Arrays.toString(Arrays.copyOfRange(x, i + 1, x.length)));
            x[i] = B_copy[i][0];
            for (int j = i + 1; j < N; j++) {
                x[i] -= A_copy[i][j] * x[j];
            }
            System.out.println("x[" + i + "]: " + x[i]);
        }

        // Resultados
        System.out.println("\nMatriz A triangularizada:");
        printMatrix(A_copy);
        System.out.println("\nVector B triangularizado:");
        printMatrix(B_copy);
        System.out.println("\nSolucion:");
        System.out.println(Arrays.toString(x));

        scanner.close(); // Cerrar el scanner
    }

    public static void printMatrix(double[][] matrix) {
        for (double[] row : matrix) {
            System.out.println(Arrays.toString(row));
        }
    }



### Ejemplos Eliminación Gaussiana

## Ejemplo 1

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/3a376ee5-0126-42d2-909c-a57c5bd2daf7)

![image](https://github.com/xlmdn/problemario/assets/147437527/230d0971-fb8d-419e-bb6f-c77479142103)


salida

![image](https://github.com/xlmdn/problemario/assets/147437527/0fc9c903-f3d8-4fa4-b0ef-63b056bd2a6d)

## Ejemplo 2

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/995e3c85-013a-49bd-ba7f-1b54ab053b2e)

![image](https://github.com/xlmdn/problemario/assets/147437527/de440c60-bdeb-4498-9737-9f8df80d89c2)


salida

![image](https://github.com/xlmdn/problemario/assets/147437527/40ad4f99-3581-4643-9553-bbd7e1524dd3)



## Ejemplo 3

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/e3706641-99e0-4b8f-8048-9e6f72b89cf8)

![image](https://github.com/xlmdn/problemario/assets/147437527/725c751e-6086-4184-9143-07dcc5589136)

salida

![image](https://github.com/xlmdn/problemario/assets/147437527/84447f21-399b-4707-aaa3-62d01fd05767)

## Ejemplo 4

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/250da839-6831-47b8-a974-6522a47e298b)

![image](https://github.com/xlmdn/problemario/assets/147437527/4a85f20a-9072-42a6-b033-f4065cc5bb71)

salida

![image](https://github.com/xlmdn/problemario/assets/147437527/d9e18a9e-1259-4801-abc4-c7d005b49b23)


## Ejemplo 5

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/a7358a9c-3f3a-4b04-ba8d-42cc1b2ea91d)

![image](https://github.com/xlmdn/problemario/assets/147437527/85b922eb-83a1-42db-81eb-2a1435ce72f9)

salida

![image](https://github.com/xlmdn/problemario/assets/147437527/e1f3ef3d-dd53-4f14-b6ab-082d3d8d3e67)


## Método Jacobi

### Descripción Jacobi

El método de Jacobi es un algoritmo iterativo utilizado para resolver sistemas de ecuaciones lineales, especialmente cuando la matriz del sistema es grande y dispersa. El método se basa en la descomposición de la matriz del sistema en una matriz diagonal y el resto de los términos.

![image](https://github.com/xlmdn/problemario/assets/147437527/db4f64b8-f9e2-4d32-abf5-75c184d62b2e)


### Algoritmo Jacobi

-Descomposición de la matriz: Separar la matriz del sistema en una matriz diagonal y dos matrices triangulares.

-Iteración inicial: Seleccionar un vector inicial de soluciones.

-Iteración: Evaluar cada una de las funciones con los valores iniciales de forma iterativa para actualizar el vector de soluciones en cada paso.

Criterio de parada: Verificar si se ha alcanzado la convergencia.

Convergencia: Si se ha alcanzado la convergencia, devolver el vector de soluciones aproximado.

# Implementación Jacobi


    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Solicitar el tamaño del sistema
        System.out.print("Ingrese el tamaño del sistema: ");
        int tam = sc.nextInt();

        // Validar el tamaño del sistema
        if (tam < 2) {
            System.out.println("El tamaño del sistema debe ser mayor o igual a 2.");
            return;
        }

        // Solicitar la matriz de coeficientes y el vector de resultados
        double[][] matrizCoeficientes = new double[tam][tam];
        double[] vectorResultados = new double[tam];

        System.out.println("Ingrese la matriz de coeficientes:");
        for (int i = 0; i < tam; i++) {
            for (int j = 0; j < tam; j++) {
                System.out.print("Ingrese el elemento [" + (i + 1) + "][" + (j + 1) + "]: ");
                matrizCoeficientes[i][j] = sc.nextDouble();
            }
        }

        System.out.println("Ingrese el vector de resultados:");
        for (int i = 0; i < tam; i++) {
            System.out.print("Ingrese el elemento [" + (i + 1) + "]: ");
            vectorResultados[i] = sc.nextDouble();
        }

        // Definir el vector inicial (se quedan en 0)
        double[] vectorInicial = new double[tam];
        double[] vectorAnterior = new double[tam];

        int maxIteraciones = 50;

        // Realizar iteraciones en el método de Jacobi
        for (int k = 0; k < maxIteraciones; k++) {
            System.out.print("Iteración " + (k + 1) + ": ");

            // Calcular nuevos valores de x
            double[] x = new double[tam];
            for (int i = 0; i < tam; i++) {
                double sum = 0;
                for (int j = 0; j < tam; j++) {
                    if (j != i) {
                        sum += matrizCoeficientes[i][j] * vectorInicial[j];
                    }
                }
                x[i] = (vectorResultados[i] - sum) / matrizCoeficientes[i][i];
            }

            double errorAbsoluto = calcularErrorAbsoluto(x, vectorAnterior);

            if (k > 0 && errorAbsoluto < 0.05) {
                System.out.println("Error absoluto menor al 5% en la iteración " + (k + 1) + ".");
                break; // Romper el ciclo
            }

            // Mostrar resultados de la iteración
            for (int i = 0; i < tam; i++) {
                System.out.printf("x%d = %.4f ", i + 1, x[i]);
            }
            System.out.println();

            // Actualizar el vector inicial y el vector anterior para la próxima iteración
            System.arraycopy(x, 0, vectorInicial, 0, tam);
            System.arraycopy(x, 0, vectorAnterior, 0, tam);
        }
    }

    private static double calcularErrorAbsoluto(double[] vectorActual, double[] vectorAnterior) {
        double maxError = 0;
        for (int i = 0; i < vectorActual.length; i++) {
            double error = Math.abs((vectorActual[i] - vectorAnterior[i]) / Math.abs(vectorActual[i]));
            maxError = Math.max(maxError, error);
        }
        return maxError;
    }



### Ejemplos Jacobi

## Ejemplo 1

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/e12652c0-3407-4fb1-84d0-fd402bc1e8d3)

![image](https://github.com/xlmdn/problemario/assets/147437527/1969ac1f-202d-41da-a533-8ac8f4a995ee)

salida

![image](https://github.com/xlmdn/problemario/assets/147437527/e1fc71c9-beff-4c26-89ee-719b8f3dd32e)

## Ejemplo 2

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/8e43e1fa-1596-4765-9be6-d25ed2423f9b)

![image](https://github.com/xlmdn/problemario/assets/147437527/308953d4-f618-405d-8d1d-86a945a4be30)

salida

![image](https://github.com/xlmdn/problemario/assets/147437527/55d82ccf-23ce-4f06-911b-cef7a84e85fe)

## Ejemplo 3

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/f0c0c570-c266-4a5e-81a6-2ff3c9b9332b)

![image](https://github.com/xlmdn/problemario/assets/147437527/31ef96ce-dd82-4381-b718-62ea7ed70582)

salida

![image](https://github.com/xlmdn/problemario/assets/147437527/df112e9f-c893-44d6-b82d-22344b88d0eb)

## Ejemplo 4

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/5f720301-4cf4-4afc-a495-d8a48b3b79e9)

![image](https://github.com/xlmdn/problemario/assets/147437527/aca01853-0948-45e8-9529-e1f26ea3248a)

salida

![image](https://github.com/xlmdn/problemario/assets/147437527/653f3ff1-9c36-4a84-a222-2ac2b0a8d049)


## Ejemplo 5

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/9544e680-3f53-4d3c-9ff4-4ed72fcb4d12)

![image](https://github.com/xlmdn/problemario/assets/147437527/51d4ea0b-fe2c-44a2-87b4-474b9ccce24e)

salida

![image](https://github.com/xlmdn/problemario/assets/147437527/d27cf32b-ba74-4bf4-af52-bb2e14ff546e)

## Contribuciones y Retroalimentación:

Este repositorio es un recurso en constante evolución, y tu contribución es fundamental para mejorarlo. Si tienes sugerencias, correcciones o nuevos recursos que te gustaría compartir, no dudes en hacer una contribución al repositorio. Además, apreciamos cualquier retroalimentación que tengas sobre tu experiencia utilizando este material.

¡Esperamos que este repositorio sea una herramienta valiosa para tu estudio y práctica de Métodos Numéricos! Si tienes alguna pregunta o necesitas ayuda adicional, no dudes en ponerte en contacto.

¡Que disfrutes explorando el mundo de los Métodos Numéricos!

Atentamente, 

Axel Madin
