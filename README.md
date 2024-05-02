
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

### Descripción Simpson tres octavos


El método de Simpson 3/8 es una técnica de integración numérica que se utiliza para aproximar el valor de una integral definida. Es una extensión del método de Simpson, que a su vez es una mejora del método del trapecio. Este método se utiliza cuando se requiere una mayor precisión en la aproximación de la integral.

La idea principal detrás del método de Simpson 3/8 es aproximar el área bajo la curva de una función mediante la interpolación de la función por medio de polinomios de grado dos. En lugar de dividir el intervalo de integración en segmentos de igual longitud como en el método de Simpson estándar, en el método de Simpson 3/8 se divide el intervalo en segmentos de longitud igual a 1/3 del ancho total del intervalo.

![image](https://github.com/xlmdn/problemarioT4/assets/147437527/2ece4245-31ea-4788-ab6a-b6a1694bb4d5)



### Algoritmo simpson tres octavos

![image](https://github.com/xlmdn/problemarioT4/assets/147437527/c597ffef-bde8-4412-884b-40ab37ba30e4)

# Implementación Eliminación Gaussiana

public static void main(String[] args) {
        // función 2x + 10 en a=1, b=3
        double a,b,f1,f2,f3,f4,res,h,c,d;
        a=1;
        b=3;
        h=(b-a)/3;
        c=a+h;
        d=c+h;
        f1=2*a+10;
        f2=2*c+10;
        f3=2*d+10;
        f4=2*b+10;
        res=(3*h/8)*(f1+3*f2+3*f3+f4);
        System.out.println("El área bajo la curva es: "+res);
    }

### Ejemplos simpson tres octavos

## Ejemplo 1


## Ejemplo 2


## Ejemplo 3

## Ejemplo 4


## Ejemplo 5





## Contribuciones y Retroalimentación:

Este repositorio es un recurso en constante evolución, y tu contribución es fundamental para mejorarlo. Si tienes sugerencias, correcciones o nuevos recursos que te gustaría compartir, no dudes en hacer una contribución al repositorio. Además, apreciamos cualquier retroalimentación que tengas sobre tu experiencia utilizando este material.

¡Esperamos que este repositorio sea una herramienta valiosa para tu estudio y práctica de Métodos Numéricos! Si tienes alguna pregunta o necesitas ayuda adicional, no dudes en ponerte en contacto.

¡Que disfrutes explorando el mundo de los Métodos Numéricos!

Atentamente, 

Axel Madin
