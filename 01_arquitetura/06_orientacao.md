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

*
