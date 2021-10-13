# Testes com Junit 4 e Junit 5

https://junit.org/junit5/

## Testes com Junit 4

### Requisitos
- IDE Eclipse (ou de sua preverência)
- JDK 8
- maven
- Junit 4.12

O Junit é um framework simples e de código aberto para testes unitários. Esses testes são para testes uma única funcionalidade do seu código Java, como por exemplo um método de uma classe. Idealmente cada classe precisa de uma classe de testes. Com o maven é criado uma organização de pastas onde estão os codigos e os seus respectivos testes.

O interessante do Junit é que a cada compilação do seu programa, ele será novamente testado e com isso é necessário que o teste passe ok sempre.

### Criando um projeto maven de exemplo

Exemplo simples na IDE Eclipse

- File -> New -> Maven Project -> Create Simple Project
- preencher:
  - Group ID: br.com.nome-relativo
  - Artifact ID: nome-projeto
  - Name: nome-projeto
  - Description: descricao do projeto

Trabalhar nas pastas:
- main/java
- test/java
- Para cada classe na pasta main, precisa de uma classe de teste
- verificar se no arquivo pom.xml está a dependência do Junit

Para criar um caso de teste do zero, é possível clicar na classe que quero testar e:
- New -> Other -> Junit Case Test -> Verificar os nomes -> escolher os métodos que serão testados

### Assertions
- Utilizados para a validação de testes
- No Junit existem assertions para tipos, primitivos, Objetos e arrays
- Possuem imports statics que facilitam a implementação no código
- Exemplos:
  - assertArraysEquals -> para arrays
  - assertEquals ->
  - assertFalse ->
  - assertNotNull ->
  - assertNotSame ->
  - assertNull ->
  - assertSame ->

### Rules


### Exceções
- Exceções esperadas:
  - Colocado qual a exceção esperada no teste

        @Test(expected = IndexOutBoundsExceptions.class)
        public void empty(){
            new ArrayList<Object>().get(0)
        }

- Exceções esperadas Rule:
  - Usando a anotação Rule

        @Rule
        public ExpectedException thrown = ExpectedException.none();

        @Test(expected = IndexOutBoundsExceptions.class)
        public void empty(){
            List<Object> list = new ArrayList<Object>();

            thrown.expect(IndexOutOfBoundsException.class);
            thrown.expectMessage("Index: 0, Size: 0");
            list.get(0);
        }

- Try/catch idiom:
  - lorem ipslum

        @Test
        public void testTryCatchIdiom() {
            try {
                new ArrayList<Object>().get(0);
                fail("Esperado que IndexOutOfBoundsException seja lançado");
            } catch (IndexOutOfBoundsException ex) {
                assertThat(ex.getMessage(), is("Index: 0, Size: 0"));
            }
        }

***

## Trabalhando com Mocks

- O que são Mocks?
  - São termos que servem para descrever objetos que simulam comportamentos de objetos reais de forma controlada. Quando criar um objeto real é mais complicado é bom utilizar um mock
  - Ex:
    - Banco de Dados
  - Limitações:
    - Lorem

- Frameworks:
  - Mockito
    - https://site.mockito.org/
  - EasyMock
    - https://easymock.org/
  - PowerMockito
    - https://www.baeldung.com/intro-to-powermock
  
- Exemplo prático com mockito:
- 

