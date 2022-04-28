# Docker envs
Ambientes Docker pré configurados para uso.

## Como utilizar:
1. Instale o Docker na sua maquina
2. Clone o projeto para sua maquina
3. Via terminal, entre no diretório onde você clonou o projeto e rode o comando docker-compose up -d
4. O Docker automaticamente vai baixar as imagens e criar os containers
5. Ambiente pronto para ser utilizado

## dev_env
Ambiente de desenvolvimento pré configurado, o docker-compose.yml possui os seguintes containers:

- php72
- php8
- mariadb
- nginx
- elasticsearch

### Nginx
Se comporta como proxy reverso, redirecionando as requisições dinamicamente para os containers php72 e php8, para configurar o Nginx alterar o arquivo dev_env/nginx/default.conf.

### php72 e php8
Ambos os containers possuem um apache cada com as suas respectivas versões do PHP, para configurar vhosts para ambos os apaches alterar o arquivo dev_env/apache/000-default.conf.

### mariadb
Possui o mysql

### elasticsearch
contém o elasticsearch 7, que é utilizado pelo site b2b
