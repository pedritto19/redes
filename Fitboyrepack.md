Aqui estão as instruções para executar um servidor TCP em Docker 

1. Para executar um servidor TCP em Docker e permitir que os usuários solicitem um arquivo HTML, siga os seguintes passos:

- Abra o Docker usando o comando "docker run" e assegure-se de que o servidor seja iniciado na porta 15674, utilizando o seguinte comando:

docker run -d -p 15674:15674 -it --rm --name <nome da empresa> -v "$PWD":/var/www/servidortctp -w /var/www/servidortctp python:2 python ./TCPServer.py

No exemplo dado, o comando é "docker run -d -p 15674:15674 -it --rm --name empresadesoftware -v "$PWD":/var/www/servidortctp -w /var/www/servidortctp python:2 python ./TCPServer.py".

2. Agora, copie o arquivo HTML que você deseja disponibilizar no Docker usando o comando "docker cp", que permitirá que você copie arquivos de um local para outro dentro do Docker. 

Use o seguinte comando:

docker cp <nome do arquivo> <nome do container>:<caminho para o qual o arquivo será copiado>

Por exemplo:

docker cp index.html armarionet:/var/www/servidortctp/

3. Para verificar se o arquivo HTML foi carregado corretamente no Docker, execute o seguinte comando:

docker exec armarionet ls /var/www/servidortctp/

4. Finalmente, para acessar o arquivo HTML, use o comando "wget" seguido do endereço IP e da porta configurada para o Docker. Substitua "<porta configurada>" pela porta configurada no comando de inicialização do Docker. 

Por exemplo, se a porta configurada for 15674, use o seguinte comando:

wget localhost:15674

