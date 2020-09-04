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