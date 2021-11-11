# Introdução a Programação Orientada a Objetos (POO)

## Diferenças entre Programação estrutura e POO

 - Várias linguagem modernas utlizam o POO

### Programação Estruturada
Não há problema nenhum nessa programação, exceto que para programas complexos, a organização do código se torna um desafio.
Ex: C, Pascal, COBOL

### Programação Orientada a Objetos (POO)
Ser uma linguagem OO, não significa que seu programa também será OO.

Primeira linguagem OO foi a Simula 67 na década de 60, pelos noruegueses Ole-Jonah Dall e Kristen Nygaard
Alguns conceitos parecidos com linguagem de hoje:
- Classes e objetos;
- Subclasses;
- Métodos virtuais;
- Frameworks;
- Concorrência;
- Gerenciamento de memória;

## Função utilitária e conceitos básicos
- Consegue resolver o problema por ela mesma, sem dependências externas
- Paremêtros de entradas simples e direto
- Resultado de sáida simples e direto

Ex: Validação de CPF, pois a entrada é simples (num de CPF), não depende de recursos externos (DB) e saída simples e direta (Verdadeiro ou falso).

Conceitos de OO:
- Classe e Objeto: Representação de dados em objetos ou entidades para o processamento de outros objetos
- Associação de Classes: Quando utilizamos uma classe dentro de outra classe
- Herança: Utilização de uma classe base, fazendo outra nova classe que tenha os atributos e funções da classe mãe, mais as suas próprias
- Encapsulamento: Possibilidade de proteger dados ou funcionalidades da classes, permitindo um controle de acesso a elas.
- Polimorfismo: Pode ser criados funções com mesmo nome, mas que podem ter diferentes processamentos ou na mesma classe o mesmo nome e diferentes entradas

Exemplo: 
```java
package poo.model

public class Pessoa{

    private static final int TAMANHO_CPF = 11;
    private static final int TAMANHO_CNPJ = 14;

    public enum TipoPessoa{ FISICA, JURIDICA}

    private Integer id;
    private String nome;
    private String documento;
    private TipoPessoa tipo;

    public String getDocumento(){

    }

    public void setDocumento(String documento){ // Polimorfismo
        if (documento == null || documento.isEmpty()){
            throw new RuntimeException("Documento não pode ser nulo ou vazio");
        }
        if (documento.length() == TAMANHO_CPF){
            setDocumento(documento, TipoPessoa.FISICA);
        } else if (documento.length() == TAMANHO_CNPJ){
            setDocumento(documento, TipoPessoa.JURIDICA);
        } else {
            throw new RuntimeException("Documento invalido para pessoa fisica ou juridica");
        }

        this.documento = documento;
    }

    private void setDocumento(String documento, TipoPessoa tipo){ // Polimorfismo
        this.documento = documento;
        this.tipo = tipo;
    }

    public TipoPessoa getTipo(){
        return tipo;
    }
}
```
```java
public class Cliente extends Pessoa{ // Herança

    private List<Endereco> enderecos; // Associação de classes

    public void adicionaEndereco(Endereco endereco){
        if (endereco == null){
            throw new NullPointerException("Endereco não pode ser nulo");
        }
        getEnderecos().add(endereco);
    }

    private List<Endereco> getEnderecos(){ // encapsulamento
        if (enderecos == null){
            enderecos = new ArrayList<Endereco>();
        }
        return enderecos;
    }
}
```
```java
package poo.model

public class Endereco{

    private enum TipoEndereco{
        RESIDENCIAL, 
        ENTREGA, 
        TRABALHO}

    private String endereco;
    private String numero;
    private String complemento;
    private String bairro;
    private String estado;
    private String cep;
}

```
