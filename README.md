# Nome do Sistema
* apidashboard API  PHP COM LARAVEL
* apidashboard FRONTEND EM REACTJS 

Observações: Este Repositório de Docker é exclusivo para o desenvolvedor subir em ambiente localhost

# Tecnologia
* PHP 7.4
* Composer
* Apache 2
* Docker
* React

```
# clonando Repositório de codigo-fonte e de docker
-- No diretorio onde o desenvolvedor irá trabalhar, criar uma basta chamada apiloginunico.
Depois entrar dentro da pasta.
-- clonar o Repositório de docker
# git clone https://gitlabbuilder.mec.gov.br/react-charts/docker.git
-- clonar o Repositório de frontend
# git clone https://gitlabbuilder.mec.gov.br/react-charts/dashboard-frontend.git
-- clonar o Repositório de backend
# git clone https://gitlabbuilder.mec.gov.br/react-charts/dashboard-backend.git
```

# Instalação /Configuracão da aplicação

Para ambientes de desenvolvimento,  deverá obrigatoriamente utilizar o docker para disponibilizar a aplicação em desenvolvimento, para isso é necessário que se tenha o docker e o docker compose instalado e executar o seguinte comando no root da aplicação.

```
# Subindo o Frontend e Backend
--1- docker-compose build
--2- docker-compose up -d

# listando os container após o build

--docker ps

# instalando as dependências do frontend

--docker-compose exec dashboard-frontend sh -c "npm install"

# executando aplicação do frontend

--docker-compose exec dashboard-frontend sh -c "npm start"

# buildando somente o frontend

---docker-compose build dashboard-frontend 
---docker-compose up -d dashboard-frontend 

# Configurando o Backend da aplicação

--docker-compose exec apipainel-api sh -c "composer install"

--docker-compose exec apipainel-api sh -c "cp .env.example .env"

--docker-compose exec apipainel-api sh -c "php artisan key:generate"

--docker-compose exec apipainel-api sh -c "php artisan migrate"

--docker-compose exec apipainel-api sh -c "php artisan db:seed"

```

# Visualizando aplicação localhost
* Backend na porta
http://localhost:7080/

* Frontend na porta 
http://localhost:7081/

# Banco de Dados em Postgres
```
#Migration para PHP e liquibase para Java
```
```
# **Observações**: para criação de tabela de banco de dados favor usar MAD (Metodologia de Administração de Dados do MEC) 
```
disponivel no Link: https://portalstic.mec.gov.br/images/pdf/normativos/CGGD_Anexo_Nomenclatura_Objetos_Banco_de_Dados.pdf

# Observações

Favor não alterar os arquivos de Configuração  dockerfile e docker-compose e chart, se necessário comunicar equipe da arquitetura da CGS.

```
# Observações ambiente windows maquina local no ambiente do MEC.
mudar encode para LF e UTF8 via visual Studio code
```

