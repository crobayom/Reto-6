# Reto-6

En este repositorio se pondran los resultados del cumplimiento del reto numero 6 (los diagramas dentro del archivo readme y la resolucion adiconal en el archivo de notebook de jupyter

##Diagramas de fluijo:

### 1. Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.

```mermaid
graph TD
1(Inicio) --> 2[n:int=1];
2[n:int=1] --> 3[Escribir n];
3[Escribir n] --> 10[Escribir espacio];
10[Escribir espacio] --> 4[Escribir n**2];
4[Escribir n**2] --> 11[Saltar de linea];
11[Saltar de linea] --> 5{¿Es n mayor que 100?};
5{¿Es n mayor que 100?} --> 6[si];
5{¿Es n mayor que 100?} --> 7[no];
6[si] --> 8(Fin);
7[no] --> 9[n+1];
9[n+1] --> 3[Escribir n];

```

### 2. Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.

(En este punto tengo dos posturas, la primera es la mas organizadita y "juiciosa" de hacer para tomar en cuenta todos los casos aunque no sean necesarios, poe si acaso luego se quierne cambiar las condiciones, para no tener que cambiar toda la lgocia, la segunda es la mas eficiente, pero tal vez un poco "hardcodeada" en mi opinion, pero por eso esta como alternativa.)

```mermaid
graph TD
1(Inicio) --> 2[n:int=1];
2[n:int=1] --> 3{n/2==0};
3{n/2==0} --> 4[si];
3{n/2==0} --> 5[no];
4[si] --> 6[n+1];
6[n+1] --> 9{¿Es n menor de 1000?};
9{¿Es n mayor de 1000?} --> 10[si];
9{¿Es n mayor de 1000?} --> 11[no];
11[no] --> 3{n/2==0};
5[no] --> 7[Escribir n];
7[Escribir n] --> 8[Escribir espacio];
8[Escribir espacio] --> 6[n+1];
10[si] --> 12[Saltar de linea];
12[Saltar de linea] --> 13[n=1];
13[n=2] --> 14{n/2==0};
14{n/2==0} --> 15[si];
14{n/2==0} --> 16[no];
16[no] --> 19{n+1};
15[si] --> 17[Escribir n];
17[Escribir n] --> 18[Escribir espacio];
18[Escribir espacio] --> 19[n+1];
19[n+1] --> 20{¿Es n menor que 1000?};
20{¿Es n mayor que 1000?} --> 21[si];
20{¿Es n mayor que 1000?} --> 22[no];
21[si] --> 23[Fin];
22[no] --> 14{n/2==0};
```

```mermaid
graph TD
1(Inicio) --> 2[n:int=1];
2[n:int=1] --> 3[Escribir n];
3[Escribir n] --> 4[n+2];
4[n+2] --> 5{¿Es n mayor a 999?};
5{¿Es n mayor a 999?} --> 6[si];
5{¿Es n mayor a 999?} --> 7[no];
6[si] --> 8[n=2];
7[no] --> 16[Escribir espacio];
16[Escribir espacio] --> 3[Escribir n];
8[n=2] --> 17[Saltar de linea];
17[Saltar de linea] --> 9[Escribir n];
9[Escribir n] --> 10[n+2];
10[n+2] --> 12{¿Es n mayor a 1000?};
12{¿Es n mayor a 1000?} --> 13[si];
12{¿Es n mayor a 1000?} --> 14[no];
13[si] --> 15(Fin);
14[no] --> 9[Escribir n];
```

### 3. Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado
(aqui tambien se podrian tomar ambas perspectivas, pero voy, 

```mermaid
graph TD
1(Inicio) --> 2[Leer el numero entero n];
2[Leer el numero entero n] --> 3{n/2==0};
3{n/2==0} --> 4[si];
3{n/2==0} --> 5[no];
4[si] --> 6[Escribir n];
5[no] --> 7[n-1];
7[n-1] --> 6[Escribir n];
6[Escribir n] --> 12[n-2];
12[n-2] --> 8{¿Es n menor que 2?};
8{¿Es n menor que 2?} --> 9[si];
8{¿Es n menor que 2?} --> 10[no];
9[si] --> 11(Fin);
10[no] --> 6[Escribir n];
```


   
