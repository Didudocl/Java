
## Sistema Unicode

- Unicode es una codificación de caracteres estándar internacional universal capaz de representar la mayoría de las lenguas escritas del mundo.

## ¿Por qué java utiliza el sistema Unicode?

- Antes de Unicode, Existían muchos estándares lingüísticos: 
    - ASCII (American Standard Code for Information Interchange) para Estados Unidos.
    - ISO 8859-1 para las lenguas de Europa Occidental.
    - KOI-8 para el ruso
    - GB18030 y BIG-5 para el chino, etc.

## Problemas

- Esto causaba dos problemas:
    - Un valor de código concreto corresponde a letras diferentes en las distintas normas lingüísticas.
    - Algunos caracteres comunes se codifican en un solo byte, mientras que otros requieren dos o más bytes.

## Solución

- Para resolver estos problemas, se desarrolló un nuevo estándar lingüístico: 
    - El sistema Unicode.
    - En Unicode, el carácter tiene 2 bytes, por lo que java también utiliza 2 bytes para los caracteres.
    - Valor mínimo: \u0000
    - Valor máximo: \uFFFF