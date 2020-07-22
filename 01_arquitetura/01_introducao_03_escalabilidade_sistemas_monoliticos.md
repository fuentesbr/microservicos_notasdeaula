# Introdução a Escalabilidade e Sistemas Monolíticos

## Sistemas Monolíticos

* Produtos
* Categorias
* Carrinho
* Ckeckout
* Busca
* Outro
* Banco de Dados

* Tudo dentro do mesmo sistemas
* Alto acoplamento
* Processo de Deploy "completo" a cada mudança
* Normalmente usa apenas uma tecnologia
* Um problema afeta todo o sistema
* Maior complexidade para times

* Não é crime algum usar sistemas Monolíticos
* Na maioria dos casos vai atender
* Menos complexidade na maioria dos casos
* Sistema monolítico é Vida!

## Escalando Software

* **Escala vertical:** aumentando recursos computacionais;
* **Escala horizontal:** adicionar mais máquinas pequenas rodando o mesmo app
(load balancer distribui as cargas);

### Escala horizontal - Detalhes sobre a arquitetura da aplicação

* **Discos efêmeros**: informações temporárias
* **Servidor de aplicação vs Servidor de assets**: separar a aplicação dos
assets (arquivos estáticos);
* **Cache centralizado / sessões centralizadas**: não fica nas máquinas, é preciso
fazer de forma centralizada;
* **Upload / Gravaçao de arquivos**: também deve estar nos assets

** TUDO PODE TER QUE SER DESTRUÍDO E CRIADO FACILMENTE!?!?!? **
