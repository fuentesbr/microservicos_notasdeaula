# Introdução ao SOLID

SOLID é um acrônimo que consolida 5 itens que são considerados como boas práticas no mundo 
do desenvolvimento orientado a objetos.

## Ágile

1. **S - SRP** - Single Responsibility Principle
2. **O - OCP** - Open-closed Principle
3. **L - LSP** - Liskov Substitution Principle
4. **I - ISP** - Interface Segregation Principle
5. **D - DIP** - Dependency Inversion Principle

# Single Responsibility Principle

Princípio da responsabilidade única - Uma classe deve ter apenas
umas responsabilidade, não deve ter coisas a mais. 

> Uma classe deve ter um, e apenas um, motivo para mudar.

## Exemplo

Classe Course - cria conexão, persiste banco de dados, cria a classe em sí;
    o certo seria para conexão, outra pra setar informações e uma para categoria;

# Open-closed Principle

Princípio do Aberto/Fechado - toda a classe deve ser aberta para extensão mas fechada para modificação.
Vai aumentando a classe, para adaptar novas funções. O certo é extender a classe, não aumentar seu tamanho.

# Exemplo

Classe vídeo com atributo tipo e um método calculaInteresse:

    Para cada nova categoria, um if diferente
    O certo é uma classe abstrada Video com uma função abstrata calculaInteresse
    Os tipos de filme serão classes extendidas de Video

# Liskov Substitution Princicple

Princípio da Substituição de (Barbara) Liskov - as subclasses podem ser substituidas pelas suas classes pai.
Em qualquer lugar do código, você pode usar a classe filho no lugar de onde normalmente é chamada a classe pai.

## Exemplo

Classe Movie com duas funções: play e increaseVolume
Classe TheLionKing extende a classe Movie.
Classe ModernTime extende a classe Movie porém é um filme mudo - está violando o principio.
    Não pode ser extendido de Movie

# Interface Segregation Principle

Princípio da Segregação de Interfaces - Uma classe não é obrigada a implementar interfaces que ela não utilizará.
Se não for utilizar todos os métodos, não deve utilizar a interface.

## Exemplo

Interface chamada Movie com dois métodos, play e increaseVolume;
Classe TheLionKing implementa os dois métodos;
Classe ModernTimes comenta pro método increaseVolume porque não será utilizada.

Soluçao: cria duas interfaces, Movie e AudioControl
    TheLionkIng implementa as duas
    ModernTimes só implementa Movie

# Dependency Inversion Principle

Princípio da Inversão de Dependência - Dependa de abstrações e não de implementações - inverter as dependencias
Uma abstração é um modelo, para não ficar preso a uma classe específica.

## Exemplo

Classe DramaCategory sem nada
Classe Movie com nome e categoria de getters e setters.
Em setCategory, o tipo é DramaCategory
    toda categoria será DramaCategory - muito acoplado

    Correto é ter uma interface Category para a categoria
    Nâo fica dependendo até a criação, a dependencia é passada na criação