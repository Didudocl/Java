
## Declaración continue de Java

- La sentencia continue se utiliza en la estructura de control del bucle cuando se necesita saltar a la siguiente iteración del bucle inmediatamente. Se puede utilizar con el bucle for o el bucle while.

- La sentencia continue de Java se utiliza para continuar el bucle. Continúa el flujo actual del programa y omite el código restante en la condición especificada. En el caso de un bucle interno, sólo continúa el bucle interno.

- Podemos utilizar la sentencia continue de Java en todo tipo de bucles como el bucle for, while y do-while.

- Sintaxis:

```Java
while(condición){
    //Declaración de salto
    continue;
}
```

- Ejemplo sentencia continue de Java:

```Java
public class example{
    public static void main(String[] args){
        //bucle for
        for(int i=1;i<=10;i++){
            if(i==5){
                //Uso declaración continue
                continue;
            }
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
6
7
8
9
10
```

- Como se puede ver en la salida anterior, 5 no se imprime en la consola. Esto se debe a que el bucle continúa cuando llega a 5.

## Sentencia continue con for interno de Java

- Continúa el bucle interno sólo si se utiliza la sentencia continue dentro del bucle interno.

- Ejemplo:

```Java
public class example{
    public static void main(String[] args){
        //bucle for externo
        for(int i=1;i<=3;i++){
            //bucle for interno
            for(int j=1;j<=3;j++){
            if(i==2&&j==2){
                //Uso declaración continue
                continue;
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
2 3
3 1
3 2
3 3
```

## Sentencia continue con bucle for etiquetado de Java

- Podemos utilizar la sentencia continue con una etiqueta. Esta característica se introdujo desde JDK 1.5. Por lo tanto, podemos continuar cualquier bucle en Java ahora si se trata de bucle externo o interior.

- Ejemplo:

```Java
public class example{
    public static void main(String[] args){
        //etiqueta aa:
        aa:
        for(int i=1;i<=3;i++){
            //etiqueta bb:
            bb:
            for(int j=1;j<=3;j++){
                if(i==2&&j==2){
                    //Uso declaración continue
                    continue aa;
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

## Sentencia continue con bucle while de Java

- Ejemplo:

```Java
public class example{
    public static void main(String[] args){
        int i=1;
        //bucle while
        while(i<=10){
            if(i==5){
                i++;
                //Uso declaración continue
                continue;
            }
            System.out.println(i);
            i++;
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
6
7
8
9
10
```

## Sentencia continue con bucle do-while de Java

- Ejemplo:

```Java
public class example{
    public static void main(String[] args){
        int i=1;
        //bucle do-while
        do{
            if(i==5){
                i++;
                //Uso declaración continue
                continue;
            }
            System.out.println(i);
            i++;
        }while(i<=10);
    }
}

```

```
Output:
1
2
3
4
6
7
8
9
10
```
