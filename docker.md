# Docker

Docker está em todas as rodas— backend, frontend, infraestrutura, devops, pesquisa academica, todo mundo quer um pouco desse mel.

O principal benefício em usar o Docker traz o interesse de todo mundo: ter um **ambiente isolado e consistente** para rodar programas de forma homogenea nos mais diversos sistemas. Sabe a piada de que "na minha máquina funciona"? É algo tão recorrente que escolheu-se dar risada para não chorar, não é um problema fácil de se resolver.

Desenvolvedores tentam instalar as mesmas versões da bibliotecas, instalar os mesmos programas, mas nem sempre o sistema da empresa roda tranquilo.
Mas por que?
Essa é a questão de 1 milhão de reais, podem haver vários motivos.
Você instalou um jogo ontem que está usando as mesmas portas, as permissões dos arquivos no disco estão bagunçadas, o `package-lock.json` na sua máquina ficou diferente e você não entende o porque, etc.
Não é incomum o seguinte cenário em pequenas e médias empresas:
> O desenvolvedor líder criou uma solução incrível(mente ruim) com 1001 sistemas de cache e mensageria e agora você, o :clown:, tem que instalar tudo isso na mão baseada na pífia documentação provida e tentar entender como configurar o ambiente.
Quando chega esse abacaxi no teu colo, você quer dar um pulo no [7º circulo do inferno de Dante](https://danteworlds.laits.utexas.edu/circle7.html) e cometer qualquer violência no primeiro cidadão que apareça na frente.
Começa a planejar quais artes você vai vender na praia.

Mas espera lá, ainda há salvação— e nós temos um meme!

![A Criação do Docker, pela Interwebs](images/meme.jpg)

Começando em 2013 e adquirindo cada vez mais adeptos, o Docker foi criado com base em funcionalidades do kernel Linux para conseguir criar um sistema isolado, mas ainda muito performático.
Agora, com o Docker, o desenvolvedor pode criar uma **receita de bolo** de um sistema, que instale as bibliotecas e serviços necessários automaticamente, e que qualquer outro desenvolvedor possa executar em suas máquinas.

No Docker, o novo sistema é executado dentro de um **container**, que significa esse isolamento entre o sistema do seu computador (**host**, hospedeiro) e o novo sistema (**guest**, hóspede).
O container tem o seu próprio sistema de arquivos, interface de rede, e lista de processos.
Por estar dentro do **host**, os processadores e memória disponíveis são limitados ao que a máquina possui.

## [Criando containers](link-sub-conteudo)

Um novo container é criado com o comando:
```bash
docker run <parametros> <imagem> <comando>
```

Esse comando irá criar um container com o sistema disponível dentro da `<imagem>`, e caso seja especificado, rodará o `<comando>` dentro do container.
Quando (e se) o comando finalizar, o container será encerrado.

Vamos rodar o comando `sleep` usando a imagem do Ubuntu:
```bash
docker run ubuntu sleep 2 
```
O que o comando `sleep` faz é esperar por N segundos (aqui, N=2), e encerrar.


```
CONTAINER ID   IMAGE    COMMAND     CREATED         STATUS                     PORTS   NAMES
125ed240be13   ubuntu   "sleep 2"   4 seconds ago   Exited (0) 2 seconds ago           condescending_banana
```

### [Usando diretorios do host](link-sub-conteudo)
### [Expondo portas](link-sub-conteudo)
## [Criando suas próprias imagens](link-sub-conteudo)
### [Somos como cebolas](link-sub-conteudo)
### [Imagem base (FROM)](link-sub-conteudo)
### [Copiando arquivos (ADD/COPY)](link-sub-conteudo)
### [Diretório atual (WORKDIR)](link-sub-conteudo)
### [Rodando comandos (RUN)](link-sub-conteudo)
### [Variaveis de ambiente (ENV)](link-sub-conteudo)
### [Argumentos (ARG)](link-sub-conteudo)
### [Comando padrão (CMD) e ponto de entrada (ENTRYPOINT)](link-sub-conteudo)
### [Multiplos estagios](link-sub-conteudo)
## [Por baixo dos panos](link-sub-conteudo)
