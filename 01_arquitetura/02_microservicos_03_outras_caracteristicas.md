# Outras Características

## Smart endpoints & dumb pipes

* Exposição de API´s (ex. Rest);
* Comunicação entre serviços;
* Comunicação síncrona e assíncrona;
* Utilização de sistemas de mensageria (ex. RabitMQ);
* Garantia de que um serviço foi ou será executado baseado na execução das filas;

## Governança descentralizada

* Ferramenta certa para o trabalho certo. Tecnologias podem ser definidas /
baseadas na necessidade do produto;
* Diferentes padrões entre _squads_: Não dá pra fazer uma mistura de diversas
tecnologias, deve haver um padrão mínimo para os times que trabalham atualmente;
* Contratos de interface de forma independente;

## Automação de infraestrutura

Agilidade na disponibilização da infraestrutura necessária. Não pode haver gargálo
nos deploys.

* Cloud computing;
* Teste automatizados;
* _Continuous delivery_;
* _Continuous integration_;
* _Load balancer / Autoscaling_;

## Desenhado para falhar

Com diversos microsserviços, é preciso projetar para que, caso um falhe, o que
acontecerá com os outros. Quais são as dependências para diminiur ou minimizar
os problemas (CEP consultado nos sites dos correios, não traz automatico,
o usuário faz o cadastro - Compra sem estoque: comprar ou não deixar comprar).
Degradar funcionalidades e criar pontos B.

* Tolerância a falha;
* Serviços que se comunicam precisam de _fallback_;
* Logging - fazer log e tudo;
* Monitoramento em tempo real;
* Alarmes;

## Design Evolutivo

* Produto bem definidos podem evoluir ou serem extintos por razões de negócio;
* Gerenciamento de versões - versões das apis para dar tempo de migração;
* _Replacement and upgradeability_: rapidamente subtitui um serviço para outro ou
fazer upgrade (Serviço do PHP para Go, deve ser fácil subtituir, os outros serviços
não devem perceber). **Serviços devem ser independentes de tecnologia**.
