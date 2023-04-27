Tutorial - Como Entrar em um Container Docker
Neste tutorial, você aprenderá como entrar em um container Docker para acessar e modificar seus arquivos. Vamos começar!

Pré-requisitos
Docker instalado na sua máquina
Um container Docker em execução
Passo 1: Listar os Containers em Execução
O primeiro passo é listar os containers que estão em execução na sua máquina. Para isso, abra o terminal e digite o seguinte comando:

docker ps


Este comando irá listar todos os containers em execução.

Passo 2: Identificar o ID do Container
O próximo passo é identificar o ID do container que você deseja entrar. O ID do container é o valor que aparece na coluna "CONTAINER ID" na lista de containers em execução.

Por exemplo:

CONTAINER ID   IMAGE      COMMAND        CREATED        STATUS        PORTS                NAMES
c3a05e9ac61f   python     "bash"         10 minutes ago Up 10 minutes 0.0.0.0:8000->8000/tcp container1


Neste caso, o ID do container é "c3a05e9ac61f".

Passo 3: Entrar no Container
Por fim, o último passo é entrar no container. Para isso, digite o seguinte comando no terminal:

docker exec -it ID-do-container bash


Substitua ID-do-container pelo ID do container que você deseja entrar.

Por exemplo, para entrar no container com o ID "c3a05e9ac61f", digite o seguinte comando:


docker exec -it c3a05e9ac61f bash


Este comando irá abrir uma sessão de terminal dentro do container, permitindo que você acesse e modifique seus arquivos.

Conclusão
Pronto! Agora você sabe como entrar em um container Docker para acessar e modificar seus arquivos. Lembre-se de que todas as modificações que você fizer dentro do container serão persistentes apenas enquanto o container estiver em execução. Se você precisar manter as modificações permanentemente, é necessário criar uma nova imagem a partir do container modificado.

