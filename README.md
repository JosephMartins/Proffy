
<h1 align="center">
  <img alt="Be The Hero" src="https://github.com/JosephMartins/proffy/blob/master/proffy-web/src/assets/images/logo.svg">
</h1>

<blockquote align="center">Projeto feito acompanhando a NLW #2</blockquote>

## :rocket: Sobre o Projeto

<p>
  O objetivo da aplicação é unir professores e alunos em uma plataforma para facilitar a comunicação entre ambos.
</p>

<br>

<h2 align="center">Estrutura do App</h2>

<h3>Web</h3>
<img src="https://github.com/JosephMartins/proffy/blob/master/gitReadme/web.png"/>
<p>
  A versão web permite que um professoor1 se cadastre, registre seus dias disponiveis e quais materias é sua especialização, criando-os com seu respectivo 
  nome,descrição e valor a aula.  
</p>

<h4>Tecnologias Utilizadas</h4>
<ul>
  <li>ReactJS</li>
  <li>Axios</li>
</ul>

<h3>Mobile</h3>
<img src="https://github.com/JosephMartins/proffy/blob/master/gitReadme/fotoefeitos.com__final_1050808787446003057_.jpg">
<p>
  Na versão para Android e Ios, conseguimos visualizar todos os proffys disponiveis, e acessar detalhes de cada um deles,
  na pagina de detalhes podemos entrar em contato com o Proffy através de seu WhatsApp ou Whatsapp.
</p>

<h4>Tecnologias Utilizadas</h4>
<ul>
  <li>React Native</li>
  <li>Expo</li>
  <li>Axios</li>
  <li>intl</li>
  <li>Feather Icons</li>
</ul>

<h3>Backend</h3>

Todo o servidor foi construido em Node com Express, usando o Knex como ORM para as migrations de comunicação com nosso banco
SQLite,usamos celebrate para as validações da requisição,e Jest para Test-driven development (TDD).

<h4 align="center">Rotas</h4>

`/sessions` - POST
```
  Recebe no body um id referente a um ONG, busca no banco de dados a Ong e retorna a Ong que 
  pertence a esse id,usada para fazer o login da sessão de uma ong.
```
`/profile` - GET
```
  Usada para listagem de dados na Web.
  Recebe uma authorization em seu Header e retorna os casos cadastrados de uma ONG específica.
```

`/incidents` - GET
```
  Usada para listagem de dados no Mobile.
  Recebe um query param que define a página que o usuario está,e retorna todos os casos.
```
`/incidents/:id` - DELETE
```
  Recebe um route param que informa o id do caso a ser deletado.
```

`/incidents` - POST
```
  Usada para criar um novo caso
  Recebe no body: title,description,value,
  Retorna o id do caso criada.
```

`/ongs` - GET
```
  Retorna todas as ongs cadastradas
```

`/ongs` - POST
```
  Usada para cadastrar uma nova ONG.
  Recebe no body: name,email,whatsapp,city,uf.
  E retorna o id da ONG criada.
```

<h4>Tecnologias Utilizadas</h4>
<ul>
  <li>NodeJS</li>
  <li>Express</li>
  <li>Jest</li>
  <li>supertest</li>
  <li>Knex</li>
  <li>SQLite</li>
  <li>cors</li>
  <li>cross-env</li>
  <li>celebrate</li>
  <li>bee-queue</li>
</ul>



<p align="center">
  <a href="#-Instalação-e-execução">Para Executar o Projeto siga o passos ABAIXO</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
</p>



Faça um clone desse repositório.

### Backend

1. Entre na pasta  `cd backend`;
2. Rode `npm install ou yarn`;
3. Rode `knex migrate ` para executar as migrations;
4. Rode `npm start ou yarn start` para iniciar o servidor.

#Frontend Web

_ps: Antes de executar, lembre-se de iniciar o backend deste projeto_

1. A partir da raiz do projeto, entre na pasta do frontend web rodando `cd frontend`;
2. Rode `npm install` para instalar as dependências;
3. Rode `npm start` para iniciar o client.

# Frontend Mobile

_ps: Antes de executar, lembre-se de iniciar o backend deste projeto_

1. A partir da raiz do projeto, entre na pasta do frontend mobile rodando `cd mobile`;
2. Rode `npm install ou yarn` para instalar as dependências;
3. Rode `npm start ou yarn start`.
4. Instale o expo no seu celular.
5. Leia o QR Code com a câmera do seu celular e espere a aplicação iniciar!


---
Feito por Joseph Martins ♥ 

