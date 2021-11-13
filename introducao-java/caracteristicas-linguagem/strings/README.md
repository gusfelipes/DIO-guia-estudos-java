# String

- Pode ser criada com a palavra reservada `String` onde ela é fortemente tipada
- Também pode ser utilizada a palavra reservada `var`, somente a partir do Java 10

```java
    String nome = "André";
    var sobreNome = "Gomes";
    final var nomeCompleto = nome + sobreNome;

    System.out.println(nome);
    System.out.println("Nome do cliente : " + nome);
    System.out.println("Nome completo do cliente : " + nomeCompleto);
    var string = new String(" Minha  String ");

// algumas métodos da classe String
    System.out.println("Char na posição : " + string.charAt(5));
    System.out.println("Quantidade=" + string.length());
    System.out.println("Sem Trim [" + string + "]");
    System.out.println("Com Trim [" + string.trim() + "]");
    System.out.println("Lower " + string.toLowerCase());
    System.out.println("Upper " + string.toUpperCase());
    System.out.println("Contém M? " + string.contains("M"));
    System.out.println("Contém X? " + string.contains("X"));
    System.out.println("Replace " + string.replace("n", "$"));
    System.out.println("Equals? " + string.equals(" Minha String "));
    System.out.println("EqualsIgnoreCase? " + string.equalsIgnoreCase(" minha sTrinG "));
    System.out.println("Substring(1,6)=" + string.substring(1, 6));
    // Pesquisar
    .toCharArray()
    .split()
    .concat()
    .replaceAll(regex)
```

## StringFormat
- Algumas maneiras de mostrar a String para o usuário e algumas formatações
```java
    var nome = "André";
    var sobreNome = "Gomes";
    final var nomeCompleto = nome + sobreNome;

    System.out.println(nome);
    System.out.println("Nome do cliente : " + nome);
    System.out.println("Nome completo do cliente : " + nomeCompleto);
    final var mensagem = String.format("O cliente %s possui sobre nome %s ", nome, sobreNome);
    System.out.println(mensagem);

    System.out.println(String.format("Numero %.2f ", 1.2375d));
```

## StringBuilder

```java
    var nome = "André";

    final var builder = new java.lang.StringBuilder(nome);
    System.out.println(builder.append("Luis"));

    final var reverse = builder.reverse();

    System.out.println(reverse);

    final var insert = reverse.insert(0, "#").insert(reverse.length(), "#");
    System.out.println(insert);
```

