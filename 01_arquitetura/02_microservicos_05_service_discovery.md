# Service Discovery

O processo de _Service Discovery_ é responsável por prover mecanismos de
identificação dos serviços disponíveis e suas instâncias.

(Descobrir os nodes e serviços que estão disponíveis)

## Service Discovery - Client Side



    /*********/    1    /***********/  <---  /* SERVICE - NODE1 */
    | CLIENT  |   --->  | SERVICE   |  <---  /* SERVICE - NODE2 */
    /*********/         | REGISTRY  |  <---  /* SERVICE - NODE3 */
        |               /***********/               /\
        |                   2                       |
        ---------------------------------------------

Nodes se registram no _SERVICE REGISTRY_ e o _client_ consulta o mesmo
para saber para qual node requisitar.

## Service Discovery - Server Side

    /*********/  
    | CLIENT  |
    /*********/
        |
        \/
    /*********/    1    /***********/  <---  /* SERVICE - NODE1 */
    | LOAD    |   --->  | SERVICE   |  <---  /* SERVICE - NODE2 */
    | BALANCER|         | REGISTRY  |  <---  /* SERVICE - NODE3 */
    /*********/         /***********/               /\
        |                   2                       |
        ---------------------------------------------

Em _Server Side_, é acrescentada um _LOAD BALANCER_ que fará a consulta no
_service registry_

## Ferramentas Populares

* Netflix Eureka
* Consul
* Etcd
* ZooKeeper
* **Kubernetes:** faz automaticamente o service discovery.
