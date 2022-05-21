## Repositório CSharp ( C# | ASP.NET Core | EF Core ) ##

=== Fundamentos ASP.NET Core / Desenvolvimento WEB / API REST / Swagger / EF Core ===

Este repositório foi criado para falar um pouco dos Fundamentos do CSharp, do ASP.NET Core, do Entity Framework, sobre desenvolvimento web, API, Swagger.

Estou estudando muito sobre a linguagem C#, sobre os Frameworks que envolvem o C#, tais como .NET, ASP.NET Core,
estou estudando muito sobre Desenvolvimento Web, APIs, etc. Pois, eu quero me tornar um Desenvolvedor Web Completo, 
então para isso, preciso ter uma base sólida. 

Sendo assim, bora estudar.. estudar.. estudar.. praticar.. praticar e estudar mais um pouco!!!
E neste sentido, vamo que vamo!!! Go.. Go.. Go

---

## Redes Sociais - Fernando Di Nardo L.

[LinkedIn - Fernando Di Nardo Lazarin](https://www.linkedin.com/in/fernando-di-nardo-lazarin-82037975/)

[Instagram - Fernando Di Nardo Lazarin](https://www.instagram.com/fernando.dinardo/)


---

### ===== Fundamentos ASP.NET Core / Desenvolvimento WEB / API REST / Swagger / EF Core =====

## 1- O que é o protocolo HTTP?

HTTP é o protocolo base de comunicação na Web, incluindo a comunicação de recursos de APIs.

---

## 2- Dê três exemplos de códigos de status HTTP.

Os status de requisição HTTP são basicamente códigos que representam o resultado de uma requição.

Os status (de SUCESSOS) HTTP mais comuns são:
200 - OK: Sucesso, geralmente retornar alguma informação.

201 - CREATED: Sucesso, geralmente retorna um objeto criado, além do caminho de detalhes dele no "location".

202 - ACCEPTED: Sucesso, indica um processamento posterior a ser executado no fluxo.

204 - NO CONTENT: Sucesso, mas sem informações de retorno.

Os status (de ERROS) HTTP mais comuns são:
400 - BAD REQUEST: Erro, indica erro nos dados da requisição.

401 - UNAUTHORIZED: Erro, indica a falta de autenticação.

404 - NOT FOUND: Erro, indica que o recurso não foi encontrado.

500 - INTERNAL SERVER ERROR: Nem queira saber o que aconteceu aqui!

---

## 3- Cite os 4 métodos HTTP mais comuns.

Uma requisição HTTP é representada por um MÉTODO, e ele representa uma ação que está sendo realizada.

Os Métodos mais comuns são:
GET, POST, PUT, DELETE.

O uso de cada uma delas deve ser guiado pelas boas práticas, 
e deve está relacionado com o padrão REST e os códigos de Status HTTP.

---

## 4- O que é o padrão REST?

REST (ou Representational State Transfer), é um padrão utilizado para comunicação entre sistemas, 
comumente utilizado com o protocolo HTTP.

E seu principal conceito é o de recurso, que representa um objeto com dados, 
o qual queremos realizar alguma operação.

URL de exemplo no padrão REST:
" api/vacancies, api/vacancies/1/apps "

---

## 5- O que são Controllers e Actions? Qual classe um Controller deve herdar?

Controllers são classes que agrupam um conjunto de ações (ACTIONS), 
e que herdam Controller ou ControllerBase. Agrupam ações de maneira lógica baseado no recurso a ser acessado.

Exemplos de Controllers:
PackagesController.cs
ApplicationsController.cs

Actions são métodos que estão contidos em um Controller, e que representam "ENDPOINTS" de uma API. 
No contexto de APIs, o retorno de uma Action geralmente é IActionResult, que nele é implementado por respostas HTTP, 
tais como o 200 (Ok), 404 (NotFound), entre outros.

As rotas e metódos HTTP utilizados são definidos através de anotações como Route, HttpGet, HttpPost, entre outras.

---

## 6- O que é o Swagger?

Swagger é uma ferramenta que simplifica o desenvolvimento de APIs permitindo, 
entre outras coisas, documentar e testar APIs.

Ele consegue gerar uma interface gráfica contendo todos os "endpoints" da API, 
permitindo realizar requisições diretamente pela sua interface.

---

## 7- O que é Injeção de Dependência? Quais os tipos de ciclos de vida de objetos existem para isso em ASP.NET Core?

Injeção de Dependências se refere a técnica em que um objeto recebe outros objetos, geralmente via Contrutores.

Instanciar diretamente objetos tem diversos problemas, como a responsabilidade de gerenciar dependências de novos objetos. 
E outro problema é uma maior dificuldade de se escrever testes unitários.

No ASP.NET Core existem 3 tempos de ciclo de vida de um objeto na injeção de dependência: "Transient", "Scoped", "Singleton".

No Singleton, a mesma instância do objeto é utilizada em todo o escopo da aplicação.
Já no Scoped, é uma utilizada uma instância para a requisição inteira.
E no Transient, é uma instância por cada uso.

---

## 8- O que é uma ORM?

ORM, ou Object-Relational Mapping, que em português é mapeamento objeto-relacional, 
é uma técnica para aproximar o paradigma de desenvolvimento de aplicações orientadas a objetos 
ao paradigma do banco de dados relacional.

---

## 9- O que é o Entity Framework Core?

O EF (Entity Framework) Core é uma versão leve, extensível, de software livre e 
multiplataforma da popular tecnologia de acesso a dados do Entity Framework.

O EF Core pode servir como um mapeador relacional de objeto (O/RM), que:

- Permite que os desenvolvedores do .NET trabalhem com um banco de dados usando objetos .NET.
- Elimina a necessidade da maior parte do código de acesso a dados que normalmente precisa ser gravado.
- O EF Core é compatível com vários mecanismos de banco de dados.

O EF Core oferece suporte a diversos banco de dados, como o SQL Server, SQLite, CosmosDB, PostgreSQL, MySQL, entre outros.

---

## 10- O que é DbContext e DbSet?

Principais conceitos do EF Core:
- Code First
- DbContext
- DbSet
- Migration

Code First significa que você deverá primeiramente escrever o código e depois você vai gerar o banco de dados.

DbContext é um contexto de dados. Ele representa como se fosse o banco de dados, 
o DbContext tem um conjunto de DbSets.

DbSet é como se fosse tabelas. Você cria um DbContext e com o contexto de dados, 
e com o DbContext você cria vários DbSets (que são as tabelas).

---

## 11- O que são Migrations?

Migration é o código que representa a alteração do estado do banco de dados. 
Por exemplo, com o Code First você primeiro escreve o código, depois cria o Banco de Dados com o DbContext e DbSets, 
e a com a Migration você irá dizer o que mudou no banco de dados, 
qual é a situação que ele irá apresentar e/ou registrar e como ele irá ficar. 
Ou seja, são migrações, são as mudanças do banco de dados.

Usando o recurso Migrations do EF, podemos realizar alterações em nosso modelo de entidades 
e ter a atualização automática do banco de dados refletindo essas mudanças.

---

## 12- Como são geradas as Migrations?

Para gerar as Migrations, existem alguns comandos:
Através de um Terminal Console e/ou CMD, pode utilizar os seguintes comandos:

dotnet ef migrations add NomeDaMigration
(Parâmetros opcionais que geralmente são utilizados: -o, -s)

dotnet ef database update
(Parâmetro opcional que geralmente é utilizado: -s)

Então, é assim:
- Add-Migration - gera o código para atualizar o banco de dados de acordo com as alterações feitas no modelo de entidades;

- Update-Database - que vai aplicar as alterações pendentes no banco de dado;

---

## 13- O que é o Padrão Repository? E qual sua importância?

O padrão Repository é um padrão que realiza a abstração do acesso aos dados da aplicação. 
Um dos principais benefícios deste padrão são a separação de responsabildiades 
e a melhoria da testabildiade através de interfaces na aplicação.

A importâcia do padrão Repository é que em qualquer aplicação de grande porte que você precisa refatorar e/ou alterar
 alguma funcionalidade você precisa utilizar a abstração e reduzir ao máximo a replicação de código. 
 Por isso é muito importante utilizar essa boa prática que é o padrão Repository.

---
In the end!
