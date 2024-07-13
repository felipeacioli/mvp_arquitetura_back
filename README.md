# API para cadastrar materiais

Este pequeno projeto é um MVP integrante da sprint I (Desenvolvimento Full Stack Básico) da pós-graduação em Engenharia de Software da PUC Rio. 

# Justicativa:

A eficiência e confiabilidade dos sistemas de automação industrial dependem, em grande parte, do pronto acesso a materiais de reposição e manutenção. Para otimizar esse processo crítico, foi desenvolvido uma API para o gerenciamento de materiais em um almoxarifado dedicado à armazenar suprimetos de reposição para manutenção em sistemas de automação industrial. 


# Funcionalidades:

Registro de materiais: a API permitirá o cadastro de materiais de reposição informando sua descrição, quantidade e grupo ao qual o material pertence;

Listar todos os materias disponíveis em estoque;


Melhorar o planejamento da manutenção ao fornecer sobre o estoque disponível.

---
## Arquitetura da Aplicação     

![image](https://github.com/user-attachments/assets/b407d9df-9708-47fb-9b74-83800db91d62)

---
## Como executar em modo Desenvolvimento:


Será necessário ter todas as libs python listadas no `requirements.txt` instaladas.
Após clonar o repositório, é necessário ir ao diretório raiz, pelo terminal, para poder executar os comandos descritos abaixo.

> É fortemente indicado o uso de ambientes virtuais do tipo [virtualenv](https://virtualenv.pypa.io/en/latest/installation.html).

```
pip install -r requirements.txt
```

Este comando instala as dependências/bibliotecas, descritas no arquivo `requirements.txt`.

Para executar a API  basta executar:

```
flask run --host 0.0.0.0 --port 5000
```

Em modo de desenvolvimento é recomendado executar utilizando o parâmetro reload, que reiniciará o servidor
automaticamente após uma mudança no código fonte. 

```
flask run --host 0.0.0.0 --port 5000 --reload
```

Abra o [http://localhost:5000/#/](http://localhost:5000/#/) no navegador para verificar o status da API em execução.


## Como executar através do Docker

Certifique-se de ter o Docker instalado e em execução em sua máquina.

Navegue até o diretório que contém o Dockerfile e o requirements.txt no terminal. Execute como administrador o seguinte comando para construir a imagem Docker:
```
docker build -t rest-api .
```
Uma vez criada a imagem, para executar o container basta executar, como administrador, seguinte o comando:

```
docker run -p 5000:5000 rest-api
```

Uma vez executando, para acessar a API, basta abrir o http://localhost:5000/#/ no navegador.

Alguns comandos úteis do Docker
Para verificar se a imagem foi criada você pode executar o seguinte comando:

```
docker images
```
### Caso queira remover uma imagem, basta executar o comando:

```
docker rmi <IMAGE ID>
```

Subistituindo o IMAGE ID pelo código da imagem

Para verificar se o container está em exceução você pode executar o seguinte comando:

```
docker container ls --all
```
Caso queira parar um conatiner, basta executar o comando:

```
docker stop <CONTAINER ID>
```
Subistituindo o CONTAINER ID pelo ID do conatiner

Caso queira destruir um conatiner, basta executar o comando:

```
docker rm <CONTAINER ID>
```
Para mais comandos, veja a documentação do docker.
