1) entrar no cedro

2)executar os comandos
nano dockerfile:
FROM python:3
ADD index.html /usr/src/app/
MORKDIR usr/src/app/
EXPOSE 8684
CMD [“python","-m","http. server”, "6968”]


3)criar imagem
docker build -f Dockerfile . -t fitboyrepack
4)run
docker run -d -p 6968:6968. --name pedrohenrique3 fitboyrepack

5)comando get
get localhost:6968 

6)testar envio do arquivo
cat index.html

