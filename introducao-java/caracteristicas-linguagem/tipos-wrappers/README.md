## Tipos primitivos
```java
// Tipos primitivos não podem ser nulos
    byte            // 8 bits
    char            // 16 bits
    short           // 16 bits
    int             // 32 bits
    int min = -2147483648;
    int max = 2147483648;
    long            // 64 bits
    long num = 16L;

    // ponto flutuantes
    float           // 32 bits
    double          // 64 bits

    // Booleano
    boolean         // True or False
```

## Wrappers
Autoboxing:

```java
    Byte b = 123;       // byte
    Short s = 123;      // short
    Integer i = 123;    // int
    Long l = 123L;      // long
    Float f = 123;      // float
    Double d = 123;     // double
    Boolean b = false;  //boolean
```

## Não primitivos
String, Number, Object e qualquer outro objeto

## Tipagem Estática
Significa que os tipos das variáveis são verificados em tempo de compilação

Tipo Inferido
Java 10
comum em outras linguagem
Significa que é possível atribuir tipos as variáveis sem definir o tipo de forma explícita
Dever ser usado a palavra reservada `var`

