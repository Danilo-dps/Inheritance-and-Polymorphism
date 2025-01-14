# Herança 

- É um tipo de associação que permite que uma classe herde todos dados e comportamentos de outra
- Vantagens
    - Reuso
    - Polimorfismo
- Sintaxe
    - class A extends B
- Herança permite o reuso de atributos e métodos (dados e comportamento)

# Definições importantes

- **Relação "é-um"**: é quando a subclasse(classe filha) passa a ser um tipo da superclasse(classe pai)
- **Generalização/especialização**: a `generalização` é o processo de definir o que vai ser em comum, para ser mantido na superclasse. A `especialização` é o processo de `herdar` as informações em comum, e adicionar o que e especifico ao seu uso.
- **Superclasse (classe base) / subclasse (classe derivada)**: A `superclasse (classe base)` é onde vai estar definido o que tem de comum, podendo ser instanciada com as suas definições, a `subclasse (classe derivada)` ao herdar, pega e acrescenta o que for o `a mais` dela, o `especifico`
- **Herança / extensão**: é a possibilidade de extender algo e reutilizar 

# Composição

- **Definição**: A composição é um tipo de associação em que uma classe é composta por uma ou mais instâncias de outras classes. Em outras palavras, uma classe contém objetos de outras classes como parte de seu estado interno. A composição representa uma relação "tem-um" ou "parte-todo".
- **Vantagens**:
    - Reuso de código
    - Modularidade
    - Flexibilidade

- **Diferenças em relação à herança**:
    - **Herança**: Relação "é-um"
    - **Composição**: Relação "tem-um"

# Definições importantes

- **Relação "tem-um"**: Quando uma classe contém instâncias de outras classes como seus atributos.
- **Agregação vs Composição**: Na `agregação`, a relação "parte-todo" é mais fraca, pois a parte pode existir independentemente do todo. Na `composição`, a parte não pode existir sem o todo. A `composição` implica em um ciclo de vida dependente.
- **Classe composta (classe todo) / classe componente (classe parte)**: A `classe composta (classe todo)` contém instâncias de outras classes, que são chamadas de `classes componentes (classes parte)`. A classe composta gerencia a existência e o ciclo de vida das classes componentes.

# Modificadores de Acesso

## Definição

Os modificadores de acesso são palavras-chave utilizadas na definição de classes, métodos e atributos para controlar a visibilidade e o nível de acesso desses elementos em relação a outras partes do código.

## Tipos de Modificadores de Acesso

- **Public**: Permite que o elemento seja acessado de qualquer outra classe.
- **Private**: Restringe o acesso ao elemento somente dentro da classe onde ele foi declarado.
- **Protected**: Permite que o elemento seja acessado por classes no mesmo pacote e por subclasses, mesmo que estejam em pacotes diferentes.
- **Default (Pacote-Privado)**: Quando nenhum modificador de acesso é especificado, o elemento é acessível apenas dentro do mesmo pacote. 

## Exemplos de Uso

```java
public class Exemplo {
    public int atributoPublico;  // Acessível por qualquer classe
    private int atributoPrivado; // Acessível apenas dentro da classe Exemplo
    protected int atributoProtegido; // Acessível por subclasses e classes no mesmo pacote
    int atributoDefault; // Acessível por classes no mesmo pacote

    public void metodoPublico() {
        // Método acessível por qualquer classe
    }

    private void metodoPrivado() {
        // Método acessível apenas dentro da classe Exemplo
    }

    protected void metodoProtegido() {
        // Método acessível por subclasses e classes no mesmo pacote
    }

    void metodoDefault() {
        // Método acessível por classes no mesmo pacote
    }
}
```

# Importância

- Os modificadores de acesso são essenciais para:
   - Encapsulamento: Protegendo os dados internos de uma classe contra acesso indevido.
   - Manutenibilidade: Facilitando a manutenção do código, ao restringir o acesso a certos métodos e atributos.
   - Segurança: Controlando quem pode ver e modificar os dados de uma classe.