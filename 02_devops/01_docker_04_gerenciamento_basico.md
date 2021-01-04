# Gerenciamento Básico de Containers

Criar um container com ngnix e rodar em background o servidor, expondo as portas.

É preciso indicar a _tag_ para baixar a image correta. Se omitir a tag, será baixada a tag _latest_.

# Expondo Portas

É preciso expor a porta, mas o container está dentro de uma rede isolada. É preciso mapear uma porta da máquina para acessar a porta do container.

# Rodando Comandos no Container

Comando docker exex nome_container para rodar comandos dentro do container. Opção -it para rodar interativamente dentro do container.

# Iniciando com Volumes

Volume permitem persistir as informações do container no host.

# Continuando com Volumes

Bind de volumes - seta um diretório do container no computador local.

# Trabalhando com Networks

Por padrão, tem 3 tipos de rede: bridge (ponte), none (nenhuma rede acessível, apenas isolado), host (o container fala
com a rede do computador).

# Docker Commit

Ao finalizar uma configuração, a gente irá criar nossas próprias imagens

# Docker Push

Envia as imagens para o repositorio próprio. è preciso rodar docker login

# Trabalhando com Dockerfile

Usado para criar containers já personalizados.

    FROM - a imagem que estamos partindo para a nossa imagem
    RUN - roda os comandos apos a máquina levantar
    COPY - copia arquivo locais para a imagem
    EXPOSE - expoe a porta do servidor
    ENTRYPOINT - o comando que irá segurar a maquina levantada
    WORKDIR - pasta inicial de trabalho

# Instalando Laravel com Dockerfile

Usou php-fpm para instalar, mas rodou o laravel no local e não na maquina vm

# Fazendo O Build De Uma Imagem com Laravel

...

# Iniciando com Docker-Compose

# Dependencia entre container

Após a versão 3 do docker-compose.yaml, as dependencias não estão mais disponíveis.

Foi apresentado o dockerize para fazer esse papel a partir da versão 3.

# Trabalhando com templates

É possível definir templates no dockerize para setar variaveis de ambiente em arquivos de configuração, como o .env por exemplo.

Importante tomar cuidado com o que vai no Dockerfile e o que vai no docker-compose.yaml, pois ao compartilhar volumes, perde o que foi feito 
no container.