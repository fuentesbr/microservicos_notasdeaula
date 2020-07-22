# API Gateway

"Uma API Gateway recebe todas as chamadas de API's dos clientes e então as
roteia para os microsserviços correspondentes..." (nginx.com)

Em alguns casos ela também é resposável por realizar processos de verificação
de segurança, como autenticação e autorização.

## Cenário de um e-commerce

    /************/      /***/
    | CLIENTES   |      | A | ---> /* CATÁLOGO  */
    /************/      | P |
                        | I |
    /* MOBILE */  --->  |   |
                        | G | ---> /* BUSCA     */
    /* DESKTOP */ --->  | A |
                        | T |
                        /***/

## Dúvida postada em Dúvidas

### API Gateway vs ESB 

Olá,

gostaria de tirar uma dúvida: a implementação da API Gateway não se assemelha muito ao Enterprise Service Bus (ESB) da Arquitetura Orientada a Serviços?

Não teríamos o problema de, caso caia, caia todos os microsserviços?
