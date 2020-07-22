# Orientação a Negócios

## Microsservices by Martin Fowler

1. Componentização via serviços

* Services dos microsserviços != Services da OO;
* "Componente é uma unidade de software independente que pode ser substituída
ou atualizada" - unidade independente que se conecta com outras unidades;
* **Desvantagens:**
    * Chamadas externas são mais custosas que locais;
    * Cruzamento entre componentes pode se tornar complexo (vender um produto
        pode gerar diversas notificações: baixa em estoque, entrega, nota fiscal);
    * Transações entre serviços são "grandes desafios" (inspeção, roll-back);
    * Mudanças bruscas em regras de negócios podem afetar diversos serviços;

2. Organização em torno do negócio

> **Conceito Importante:** Um projeto é baseado em um ou mais produtos que trabalham
> em diferentes contextos - decisões devem ser tomadas no contexto do negócio
> não no contexto técnico

* **Time de desenvolvedores por produto:** um time tem mais de um serviço, porém
entrega um produto - pensar no negócio
* **Squads:** muitas empresas tratam os times como _squads_
* **Multidisciplinar:** cada _squad_ é muito disciplinar
* **Produto:** cada _squad_ é responsável por um ou mais produtos
* **Diversos serviços:** cada produto pode ter mais de um serviço (checkout de
    e-commerce: gerenciamento de produtos, estoque, entrega)


    SQUAD POR PRODUTO

    /* SCRUM MASTER */                      /* DEVELOPER */
                        /************/
    /* TESTER */        | PRODUTO    |      /* DESIGNER */
                        /************/

                    /* PRODUCT OWNER */

**SEMPRE PENSANDO NO NEGÓCIO - PRODUTO**
