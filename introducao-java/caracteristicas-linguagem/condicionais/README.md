# Condições

## IF-ELSE
```java
    final var condicao = false;

    if (condicao)
      System.out.println("Uma única linha...");

    if (condicao) {
      System.out.println("A condição é verdadeira");
    } else {
      System.out.println("A condição é falsa");
    }

    final var ternario = condicao ? "é verdadeira" : "é falsa";

    System.out.println(ternario);
```

## SWITCH-CASE

# Operadores

## Operadores de Igualdade
(Igualdade)
- == 
- `String.equals("")`

(Desigualdade)
- !=
- `!String.equals("")`
- 
## Operadores de Incremento e Decremento
Funciona para Soma e Subtração

```java
    var numero = 1;

    System.out.println(++numero); // incrementa antes de mostrar
    System.out.println(numero++); // incrementa depois de mostrar

    var variavel = 10;

    System.out.println(--variavel);
    System.out.println(variavel--);
```

## Operadores de Lógicos
Para fazer operações booleanas de E (&&) ou OU (||)

```java
    final var numero = 2;
    final var letra = "A";

    //Sort Circuit
    if (numero < 5 && letra.equals("A")) {
      System.out.println("Atendeu a condição");
    }

    if (numero < 5 || letra.equals("A")) {
      System.out.println("Atendeu a outracondição");
    }

    if ((10 - 5) > 1 && (5 - 3) > 1) {
      System.out.println("Lógica maluca...");
    }

    // não é recomendado utilizar
    //Non Sort Circuit
    /*if (verifica(15) | verifica("A")) {
        System.out.println("OK");
    } else {
        System.out.println("Não OK");
    }*/

  }

  private static boolean verifica(String letra) {
    System.out.println("Verificando letra...");
    return letra.equals("A");
  }

  private static boolean verifica(Integer numero) {
    System.out.println("verificando numero...");
    return numero > 10;
  }
```
## Operadores de Matemáticos
```java
    System.out.println(0 + 1); // Soma

    System.out.println(3 - 1); // Subtração 

    System.out.println(3 * 1); // Multiplicação

    System.out.println(8 / 2); // Divisão

    System.out.println(8 % 2); //módulo - resto da divisão

    // maneira resumida para atribuir o novo valor para a mesma variável
    var numero = 10;
    numero *= 2;
    System.out.println(numero);
```

## Operadores de Relacionais
Relação entre valores de maior, menor ou igual
```java
    final var numero = 6;

    if (numero > 20) {
      System.out.println("O número é maior que 20");
    } else if (numero >= 10) {
      System.out.println("O número é maior ou igual a 10");
    } else if (numero <= 5) {
      System.out.println("O número é menor ou igual que 5");
    } else {
      System.out.println("nenhuma da anteriores");
```
