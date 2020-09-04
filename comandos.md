# WSL

    wsl --list 
        // lista as imagens registradas
    
    wsl --export NomeDaImagem Local 
        // exporta a imagem para o local. 
        // Ex: wsl --export Ubuntu-20.04 'D:\WSL\Ubuntu-20.04.tar'
    
    wsl --unregister NomeDaImagem 
        // remove a imagem do registro
    
    wsl --import NomeDaImagem Local 
        // registra a imagem em novo local. 
        // Ex: wsl --import Ubuntu-20.04 'D:\WSL\' 'D:\WSL\Backup\Ubuntu-20.04.tar'

# Docker

    docker run imagem:tag
        // roda a imagem escolhida. caso a tag seja suprimida, pega a _latest_
        // -d - roda em background
        // --name nomear o container
        // -p - indicar a porta que será mapeada para o container - PORTA_HOST:PORTA_CONTAINER
        // -v - indica o caminho para os volumes LOCAL_HOST:LOCAL_CONTAINER
        // --net - indica a rede 

    docker stop/start
        // para inicia o container
    
    docker ps
        // lista os containers que estão rodando
        // -a - mostra todos os containers já rodados

    docker rm ID/Name
        // remove um container pelo id ou nome randomico
        docker rm $(docker ps -aq) -f //lista dos os hashs do docker e para para o rm -f

    docker images
        // lista as imagens que estão no cache

    docker rmi ID
        // -f força a remoção da imagem;
        //remove as imagens em cache
        //dá erro caso a imagem esteja sendo utilizada em um container, mesmo parado

    docker exec NOME_CONTAINER COMANDO
        // roda comandos dentro do container
        // -it - roda interativamente dentro do container

    docker volume
        // ls - lista os volumes
        // create - criar colume
        // inspect NOME_VOLUME - dados do volume

        docker volume create --driver local --opt type=none --opt device=$(pwd) --opt o=bind volume_local

    docker network
        // ls - lista as redes
        // inspect NOME_REDE - dados da rede
        // create - criar rede

    docker commit ID NOME

    docker login

