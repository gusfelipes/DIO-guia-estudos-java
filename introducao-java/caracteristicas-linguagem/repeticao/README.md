# Laços de Repetição

## FOR
- condição inicial
- condição de avaliação a cada intereção
- o que fazer a cada interação

```java
    for (int i = 0; i <= 10; i = i + 1) {
      System.out.println("I=" + i);
    }

    for (int x = 0; x <= 5; x++)
      System.out.println("X=" + x);
```

## WHILE
Duas Variações

```java
    var x = 0;

    //Testa a condição antes
    while (x < 1) {
      System.out.println("Dentro do while...");
      x++;
    }

    var y = 0;

    //Testa a condição depois
    do {
      System.out.println("Dentro do do/while...");
    } while (y++ < 1);
```

