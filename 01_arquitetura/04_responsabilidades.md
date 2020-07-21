# Distribuição de Responsabilidades

Desenvolver software delegando responsabilidades.

**Aplicação**


    /* PROXY REVERSO  */        /*--------------*/      /*    DB        */
                                |               |   
                                |     APP       |
                                |               |    
    /*    ELASTIC     */        /*--------------*/      /*   CACHE      */

                                /* STATIC-ASSETS */

Uma vez elaborado dessa forma, podemos diversificar as máquinas do APP para
outras máquinas.


                            /*------*/   /*------*/     /*    DB    */
    /* PROXY REVERSO  */    |  APP1 |    |  APP2 |   
                            /*-----*/    /*-----*/  

                            /*------*/   /*------*/
    /*    ELASTIC     */    |  APP3 |    |  APP4 |      /*   CACHE  */
                            /*-----*/    /*-----*/

                            /* STATIC-ASSETS */

Diversas máquinas podem ser acionadas para dar vazão à demanda pelo app, já que
as responsabilidades estão mais distribuídas.

** ...mas, ainda assim, trata-se de uma aplicação monolítica. **

## Como escalar horizontalmente aplicações monolíticas

* Ter imagens / containers
* Ser facilmente reconstruída
* Ter suas responsabilidades, incluindo assets, etc
* Sim, aplicações monolíticas podem ser totalmente escaláveis

## Quando as aplicações monolíticas podem parar de valer a pena?

* **Times grandes:** muitos conflitos no git;
* **Escalar sistema:** escalar todo o sistema quando apenas uma área específica
esteja em pico de utilização;
* **Riscos:** risco de um deploy completo começa a se elevar - todo mundo
acessando o catálogo, porém uma mexida errada na área administrativa derruba
todo o sistema;
* **Tecnologias:** necessidade de utilizar tecnologias diferentes;
