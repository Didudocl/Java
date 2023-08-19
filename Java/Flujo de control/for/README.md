
## Bucle for de Java

- Se utiliza para iterar una parte del programa varias veces. Si el número de iteraciones es fijo, se recomienda utilizar el bucle for.

- Hay tres tipos de bucles for en Java:

    - Bucle for simple.

    - Bucle for-each o bucle for mejorado.

    - Bucle for etiquetado.

## Bucle for simple

- Un bucle for simple es igual que en C/C++.

- Podemos inicializar la variable, comprobar la condición e incrementar/decrementar el valor.

- Consta de cuatro partes:

    - Inicialización: Es la condición inicial que se ejecuta una vez cuando comienza el bucle. Aquí podemos inicializar la variable, o podemos utilizar una variable ya inicializada. Es una condición opcional.

    - Condición: Es la segunda condición que se ejecuta cada vez para probar la condición del bucle. Continúa la ejecución hasta que la condición es falsa. Debe devolver un valor booleano verdadero o falso. Es una condición opcional.
 
    - Incremento/Decremento: Incrementa o decrementa el valor de la variable. Es una condición opcional.

    - Sentencia: La sentencia del bucle se ejecuta cada vez hasta que la segunda condición es falsa.

- Ejemplo:

```Java
for(Inicialización,condición,Incremento/Decremento){
    //Declaración o código a ejecutar
}
```

-Ejemplo:

```Java
public class example{
    public static void main(String[] args){
        for(int i=1;i<=10;i++){
            System.out.println(i);
        }
    }
}
```

```
Output:
1
2
3
4
5
6
7
8
9
10
```

## Bucle for anidado en Java

- Si tenemos un bucle for dentro de otro bucle, se conoce como bucle for anidado.

- El bucle interno se ejecuta completamente cada vez que se ejecuta el bucle externo.

-Ejemplo:

```Java
public class example{
    public static void main(String[] args){
        for(int i=1;i<3;i++){
            for(int j=1;j<=3;j++){
            System.out.println(i+" "+j);
            }
        }
    }
}
```

```
Output:
1 1
1 2
1 3
2 1
2 2
2 3
3 1
3 2
3 3
```

- Ejemplo piramide 1:

```Java
public class example{
    public static void main(String[] args){
        for(int i=1;i<=5;i++){
            for(int j=1;j<=i;j++){
            System.out.print("* "); //El print imprimirá el mensaje en la misma línea
            }
            System.out.println(); //El println imprimirá en consola con un salto de línea
        }
    }
}
```

```
Output:
* 
* * 
* * * 
* * * * 
* * * * * 
```

- Ejemplo piramide 2:

```Java
public class example{
    public static void main(String[] args){
        int term = 6;
        for(int i=1;i<=term;i++){
            for(int j=term;j>=i;j--){
            System.out.print("* "); //El print imprimirá el mensaje en la misma línea
            }
            System.out.println(); //El println imprimirá en consola con un salto de línea
        }
    }
}
```

```
Output:
* * * * * * 
* * * * * 
* * * * 
* * * 
* * 
* 
```

## Bucle Java for-each

- El bucle for-each se utiliza para recorrer matrices o colecciones en Java. 

- Es más facil de usar que el simple bucle for porque no necesitamos incrementar el valor y utilizar la notación de subíndice.

- Funciona en base a los elementos y no al índice. Devuelve los elementos uno a uno en la variable definida.

- Sintaxis:

```Java
for(tipo de dato / variable : nombre arreglo){ //por lo general se le coloca cualquier nombre al "variable"
    //Ejecución código
}
```

- Ejemplo:

```Java
public class example{
    public static void main(String[] args){
        //Declaración arreglo
        int arr[] = {1,3,5,7,9}
        //Mostrar por pantalla los numeros del arreglo con for-each
        for(int i: arr){
            System.out.println(i);
        }
    }
}
```

```
Output:
1
3
5
7
9
```

## Bucle for etiquetado en Java

- Podemos tener un nombre de cada bucle for de Java. Para ello, utilizamos la etiqueta antes del bucle for.

- Es útil cuando se utiliza el bucle for anidado ya que podemos romper/continuar un bucle for específico.

- Sintaxis:

```Java
for(Inicialización; Condición; Incremento/Decremento){
    //Ejecución código
}
```

- Ejemplo (break aa;):

```Java
public class example{
    public static void main(String[] args){
        aa:  //etiqueta for exterior
        for(int i=1;i<=3;i++){  
            bb:  //etiqueta for interior
                for(int j=1;j<=3;j++){  
                    if(i==2&&j==2){  
                        break aa;  
                    }  
                    System.out.println(i+" "+j);  
                }  
        }  
    }
}
```

```
Output:
1 1
1 2
1 3
2 1
```

- Si utiliza break bb;, sólo se romperá el bucle interno, que es el comportamiento por defecto de cualquier bucle.

- Ejemplo (break bb;):

```Java
public class example{
    public static void main(String[] args){
        aa:  //etiqueta for exterior
        for(int i=1;i<=3;i++){  
            bb:  //etiqueta for interior
                for(int j=1;j<=3;j++){  
                    if(i==2&&j==2){  
                        break bb;  
                    }  
                    System.out.println(i+" "+j);  
                }  
        }  
    }
}
```

```
Output:
1 1
1 2
1 3
2 1
3 1
3 2
3 3
```

## Bucle for infinito en Java

- Si utiliza dos puntos y coma ;; en el bucle for, será un bucle for infinito.

- Sintaxis:

```Java
for(;;){
    //Ejecución código
}
```

- Ejemplo:

```Java
public class example{
    public static void main(String[] args){
        for(;;){
            System.out.println("Infinito");
        } 
    }
}
```

```
Output:
Infinito
Infinito
Infinito
Infinito
Infinito
Infinito
.
.
.
.
```

- Tip: Para detener la ejecución ctrl + c.

