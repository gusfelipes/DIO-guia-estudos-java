## Modificadores de Acesso

public
 - Pode ser acessada de qualquer lugar por qualquer entidade que possa visualizar a classe a que ela pertence

private
- Os métodos e atributos da classe definidos como privados não podem ser acessados ou usados por nenhuma outra classe. Nem pelas classes herdadas

protected
- Torna o membro acessível as classes do mesmo pacotes ou através de herança, seus membros herdados não são acessíveis a outras classes fora do pacote em que foram declarados

default
- A classe e/ou seus membros são acessíveis somente pelo mesmo pacote e não pela herança


abastract
- Usado somente em classes e métodos.
- Uma classe abstrata não pode ser instanciada.
- Se um método na classe for abstrato, ela tbm deve ser abstrata
Ex:
```java
    public abstract class FormaGeometrica{

        public abstract String nome(); // não tem corpo 
        public abstract Double area();

        public String desenha(int x, int y){
            return "Desenhando mas coordenadas X= " + x + " Y= " + y;
        }
    }
```

static
- Usado para criação de variáveis para ser acessada em todas as instâncias do objeto


final
- usado em métodos e variáveis
- não pode ser alterado
