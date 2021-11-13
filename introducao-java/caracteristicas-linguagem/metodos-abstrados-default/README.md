## Métodos abstratos, default e herança múltipla

### Interface
Métodos abstratos:
- Devem ser implementados por todos
- Novos métodos quebram as implementações

Métodos default:
- São herdados a todos que implementam
- Novos métodos não quebram as implementação

Pode ocorrer herança multiplas para uma interface

### Enums
- São dicionários de dados imutável
- Não é permitido criar novas instâncias
- O Construtor é sempre declarado como private
- Por convenção, como são objetos constantes e imutáveis (static final), os nomes são colocados em MAIÚSCULOS
- Possui a palavra reservada enum
- Acesso de forma estática

```java

public enum TipoVeiculo{
    TERRESTRE,
    AQUATICO,
    AEREO;
}

```

```java

public enum Status{
    OPEN(cod:13, texto: "Aberto"),
    CLOSE(cod:02, texto: "Fechado");

    private int cod;
    private String texto;

    Status(final int cod, final String texto){
        this.cod = cod;
        this.texto = texto;
    } 

    public int getCod(){return cod;}

    public String getTexto(){return texto;}
}

```