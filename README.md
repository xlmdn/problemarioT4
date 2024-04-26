
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


## Método Gauss Seidel

- [Descripción](#descripción-gauss-seidel)
- [Algoritmo](#algoritmo-gauss-seidel)
- [Ejemplos](#ejemplos-gauss-seidel)
- [Implementación](#implementación-gauss-seidel)

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

## Ejemplos Trapecio

## Ejemplo 1



## Ejemplo 2



## Ejemplo 3

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/a902a0f5-fe5b-41a5-97d5-f84553d87c86)

![image](https://github.com/xlmdn/problemario/assets/147437527/ea0a7857-abd1-4b31-9297-7f0ec1222bea)


salida

![image](https://github.com/xlmdn/problemario/assets/147437527/c0600fdb-042d-466a-9ce1-80e6d9009b4b)

## Ejemplo 4

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/c96cf10c-6258-4ec2-ad62-a2247e053429)

![image](https://github.com/xlmdn/problemario/assets/147437527/871cef1d-64ba-497c-8eec-bd89f7380da3)

salida

![image](https://github.com/xlmdn/problemario/assets/147437527/bd345a8e-5748-4fea-b660-cd2f8a056d51)

## Ejemplo 5

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/f8e099db-8760-482f-829b-9b7d206077f6)

![image](https://github.com/xlmdn/problemario/assets/147437527/61f04ce2-a730-4508-85b2-a009b85f0882)

salida

![image](https://github.com/xlmdn/problemario/assets/147437527/c2de7af7-329f-4702-ba19-7b094c5e04c0)







## Método Gauss Seidel

### Descripción Gauss Seidel

El método de Gauss-Seidel es un algoritmo iterativo utilizado para resolver sistemas de ecuaciones lineales. Su objetivo es encontrar las soluciones aproximadas del sistema iterando a través de cada ecuación y actualizando las incógnitas en cada paso. 

![image](https://github.com/xlmdn/problemario/assets/147437527/e1202242-9365-4d07-8471-8bb3943e292f)


### Algoritmo Gauss Seidel

-Inicialización: Establecer una estimación inicial para las incógnitas.

-Iteración:

Para cada ecuación del sistema:

Resolver la ecuación utilizando las incógnitas actualizadas.

Actualizar las incógnitas con los nuevos valores calculados.

Repetir hasta convergencia.

-Condición de Convergencia: Verificar si se alcanza una convergencia aceptable.

-Salida: Tomar las soluciones aproximadas como soluciones del sistema.

## Implementación Gauss Seidel



    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el tamaño de la matriz y el vector de resultados: ");
        int n = scanner.nextInt();

        double[][] matrizA = new double[n][n];
        double[] vectorB = new double[n];

        System.out.println("Ingrese los elementos de la matriz A:");
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                matrizA[i][j] = scanner.nextDouble();
            }
        }

        System.out.println("Ingrese el vector de resultados b:");
        for (int i = 0; i < n; i++) {
            vectorB[i] = scanner.nextDouble();
        }

        System.out.println("Matriz A:");
        imprimirMatriz(matrizA);

        System.out.println("Vector b:");
        imprimirVector(vectorB);

        double[] vectorX = new double[n];
        double[] vectorXNuevo = new double[n];
        int maxIteraciones = 1000;
        double tolerancia = 1e-6;

        for (int iteracion = 0; iteracion < maxIteraciones; iteracion++) {
            for (int i = 0; i < n; i++) {
                double suma = 0.0;
                for (int j = 0; j < n; j++) {
                    if (j != i) {
                        suma += matrizA[i][j] * vectorXNuevo[j];
                    }
                }
                vectorXNuevo[i] = (vectorB[i] - suma) / matrizA[i][i];
            }
            if (norma(restar(vectorXNuevo, vectorX)) < tolerancia) {
                vectorX = vectorXNuevo.clone();
                break;
            }
            vectorX = vectorXNuevo.clone();
        }

        System.out.println("La solución al sistema de ecuaciones es:");
        imprimirVector(vectorX);
    }

    public static double norma(double[] v) {
        double suma = 0.0;
        for (double num : v) {
            suma += num * num;
        }
        return Math.sqrt(suma);
    }

    public static double[] restar(double[] v1, double[] v2) {
        int n = v1.length;
        double[] resultado = new double[n];
        for (int i = 0; i < n; i++) {
            resultado[i] = v1[i] - v2[i];
        }
        return resultado;
    }

    public static void imprimirMatriz(double[][] matriz) {
        for (double[] fila : matriz) {
            for (double num : fila) {
                System.out.print(num + " ");
            }
            System.out.println();
        }
    }

    public static void imprimirVector(double[] vector) {
        for (double num : vector) {
            System.out.print(num + " ");
        }
        System.out.println();
    }



### Ejemplos Gauss Seidel

## Ejemplo 1

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/5f447999-4ab3-4b51-bbf2-3eda3a3e8539)

![image](https://github.com/xlmdn/problemario/assets/147437527/d4517535-3b2d-48c6-8194-a6e7a059d19e)

salida

![image](https://github.com/xlmdn/problemario/assets/147437527/d521dd63-e3c0-42ca-b1c4-f52e6e03ecbc)

## Ejemplo 2

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/d7eca18d-8ee3-4b0a-8772-3e46aa647eeb)

![image](https://github.com/xlmdn/problemario/assets/147437527/423c58fd-8da7-400b-aa16-e4ce2dc21a25)


salida

![image](https://github.com/xlmdn/problemario/assets/147437527/2471c22f-0f4b-4155-9bc8-04f6e2f68c75)

## Ejemplo 3

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/2e8d78e6-728a-4ab0-bcb1-bd9b267d4805)

![image](https://github.com/xlmdn/problemario/assets/147437527/554bec45-0e89-4eae-a0dc-6bd44bd3786a)


salida

![image](https://github.com/xlmdn/problemario/assets/147437527/c012cc3a-939e-4fd8-b3b4-e452308978e4)

## Ejemplo 4

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/77bfcce2-8244-49e2-a5b5-c0c8ef0f1364)


![image](https://github.com/xlmdn/problemario/assets/147437527/cc748e25-01de-4f41-be38-3721190988df)


salida

![image](https://github.com/xlmdn/problemario/assets/147437527/6475cd9e-7549-4422-9c7d-dd363a5414df)


## Ejemplo 5

entrada

![image](https://github.com/xlmdn/problemario/assets/147437527/baa3dae9-87d1-40c8-962e-247f84b41eda)

![image](https://github.com/xlmdn/problemario/assets/147437527/22c8ef2b-5cc5-4131-9183-67dde584441b)

salida

![image](https://github.com/xlmdn/problemario/assets/147437527/29e55634-2f44-45e3-b1e5-f17a32b5088f)


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
