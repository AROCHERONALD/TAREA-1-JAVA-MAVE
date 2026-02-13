# Investigación: Arreglos en Java
## Introducción
En Java, los arreglos son una de las estructuras de datos más básicas y utilizadas. Permiten almacenar múltiples elementos del mismo tipo en una sola variable y acceder a ellos mediante índices. Esta investigación describe cómo se declaran, manipulan y recorren los arreglos, así como sus diferencias con la clase `ArrayList`.

---

## 4.1 ¿Cómo se declara un arreglo en Java?
Un arreglo en Java es una estructura de datos de tamaño fijo que almacena elementos del mismo tipo. El tamaño del arreglo se define al momento de su creación y no puede modificarse posteriormente.
Existen varias formas de declarar e inicializar un arreglo en Java.

### Declaración con tamaño fijo
```java
int[] numeros = new int[5];
numeros[0] = 10;
numeros[1] = 20;
numeros[2] = 30;
```

### Declaración e inicialización directa
```java
int[] valores = {1, 2, 3, 4, 5};
```

---

## 4.2 Métodos y utilidades principales para arreglos
La clase `java.util.Arrays` es una clase utilitaria que proporciona métodos estáticos para facilitar la manipulación de arreglos en Java.

```java
import java.util.Arrays;
```

### Arrays.sort()
```java
Arrays.sort(valores);
```

### Arrays.binarySearch()
```java
int posicion = Arrays.binarySearch(valores, 3);
```

### Arrays.copyOf()
```java
int[] copia = Arrays.copyOf(valores, valores.length);
```

### Arrays.fill()
```java
Arrays.fill(numeros, 0);
```

### Arrays.equals()
```java
boolean sonIguales = Arrays.equals(valores, copia);
```

---

## 4.3 ¿Cómo se recorren los arreglos en Java?
Recorrer un arreglo en Java significa acceder a cada uno de sus elementos para leerlos o procesarlos.

### For tradicional (con índices)
```java
for (int i = 0; i < valores.length; i++) {
    System.out.println(valores[i]);
}
```

### For-each
```java
for (int numero : valores) {
    System.out.println(numero);
}
```

### Uso de Streams
```java
Arrays.stream(valores)
      .forEach(valor -> System.out.println(valor));
```

---

## 4.4 Diferencias entre arreglos y ArrayList en Java
### Arreglos
- Tamaño fijo
- Tipos primitivos y objetos
- Mejor rendimiento

### ArrayList
- Tamaño dinámico
- Solo objetos (autoboxing)
- Más flexible

```java
import java.util.ArrayList;

ArrayList<Integer> lista = new ArrayList<>();
lista.add(10);
lista.add(20);
```

---

## Conclusión
Los arreglos son ideales cuando el tamaño es conocido y se busca rendimiento, mientras que `ArrayList` es mejor cuando se requiere flexibilidad.
