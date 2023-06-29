#Criar Imagem:
->docker build -t nomeserverweb:1.0 .

#Criar container com a imagem (pra acessar usando localhost):
->docker container run --name NomeDoServidor -p 8081:80 -d seu_user_do_dockerhub/nomeserverweb:1.0

#Eviando sua imagem pro docker hub:
->docker login

->docker images #usa esse comando pra ver o ID da sua imagem

->docker tag IdQueVoceViu seu_user_do_dockerhub/nomeserverweb:1.0

->docker push seu_user_do_dockerhub/nomeserverweb:1.0

*recomendo usar esses dois comandos pra apagar qualquer container ou imagem que ja tenha na sua maquina pra não conflitar portas*
docker rm -f $(docker ps -aq) --cima exclui container
docker rmi -f $(docker images -aq) --exclui imagens

                      docker compose

docker compose up -d
![image](https://github.com/MaryBrachini/IDS/assets/92119838/d0f57d7d-2ac0-4555-bb37-133fa52b3395)
ai esse build dentro do docker compose serve pra apontar aonde ta o Dockerfile

![image](https://github.com/MaryBrachini/IDS/assets/92119838/5300c5e7-6eba-41b7-966a-e1605819759b)
pq o docker compose tbm precisa do dockerfile, no caso ai dentro tem um php com apache

![image](https://github.com/MaryBrachini/IDS/assets/92119838/1c33f9c2-c9c2-4bc4-a830-3d7748bacd41)
ai dentro de services vc tbm pode instalar o que ele pedir

*alias esse php:8.1-apache é uma imagem pronta do dockerhub que ja vem com os dois pra ficar mais leve e mais facil de instalar*

![image](https://github.com/MaryBrachini/IDS/assets/92119838/c5625471-8855-43e1-9b4b-23f6b0049301)

ele tinha pedido nginx com php ai tu tinha que procurar uma imagem com isso
![image](https://github.com/MaryBrachini/IDS/assets/92119838/7ccf255c-828c-484e-a9cc-2287d90dae14)
eu usei esse aqui, que tu coloca no RUN

![image](https://github.com/MaryBrachini/IDS/assets/92119838/33bc0774-689e-48b3-b108-9d1790e5b5d7)
esse aqui no copy, depois de você ter especificado qual pasta que da os arquivos de php

![image](https://github.com/MaryBrachini/IDS/assets/92119838/70c4ab5f-0f11-4415-862b-9f7a4e5018f1)
e o comando do cmd tu ve aqui

![image](https://github.com/MaryBrachini/IDS/assets/92119838/32486903-ae12-4e16-b5a2-27faf328c939)


https://github.com/HenriqueHyonemoto/Trabalho-Docker-IDS/blob/main/Dockerfile



