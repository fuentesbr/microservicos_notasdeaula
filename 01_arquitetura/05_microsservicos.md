# Introdução aos Microsserviços

## O que é um serviço?

* Disponibiliza Informação
* Realização de transações
* Resolve problemas de um Negócio
* Independente de tecnologia ou produto
* Pode estabelecer comunicação com diversos "clientes"

## SOA: Arquitetura Orientada a Serviços

    /* SISTEMA */       /* USUÁRIOS */
        /\                  /\
        |                   |
       \/                  \/
    /*************************************/     * Serviços baseados em funcionalidades
    | ENTERPRISE SERVICE BUS              |
    /**************************************/    * Necessidade do ESB
        /\              /\          /\          
        |               |           |           * Single point of failure
        \/              \/          \/              se o ESB cair, todo mundo cai
    /* SERVIÇO */  /* SERVIÇO */  /* SERVIÇO */
    /\              /\          /\              * Compartilhamento de Bancos de dados é comum
    |               |           |               
    \/              \/          \/              * Muitas vezes sistemas monolíticos
    /*******************************/               sendo utilizados como serviços
    |           BANCO DE DADOS      |
    /********************************/

## Arquitetura baseada em Microsserviços

**Importante:** cada serviço com um BD -  não vários serviços com um BD só como
no SOA.

    /* SITE */          /* SISTEMA INTERNO */   * Serviços pequenos com poucas
         |                          |               responsabilidades
        \/                          |
    /* SERVIÇO (BD) */              |           * Maior tolerância a falhas
         |  /\                      |
        \/  |                      \/           * Totalmente independentes
    /* SERVIÇO (BD) */ -->  /* SERVIÇO (BD) */      sozinho, consegue resolver os problemas
        |  /\                    |  /\              para o qual foi criado (BD, autenticação, deploy)
       \/  |                    \/  |
    /* SERVIÇO (BD) */      /* SERVIÇO (BD) */  * Comunicação síncrona ou assíncrona
                                                    entre microsserviços

## Microsserviços não são para todas as aplicações

* **Arquitetura complexa:** gera uma arquitetura mais complexa (muitos Sistemas
para administrar)
* **Custo:** custos mais elevados devido a muitos requisitos para cada microsserviço;
* **Equipes:** necessidade de mais equipes - squads (equipes para cada sistema);
* **Tamanho:** os sistemas precisam ser grandes o suficiente para poder quebrar
em tamahos menores;
* **Novos problemas:** novos problemas surgirão (sincronização de transações,
mensageria, equipes, etc.);
* **Monitoramento:** mais complexo;

**MICROSSERVIÇOS NÃO SÃO MODA - SÃO NECESSIDADES**
