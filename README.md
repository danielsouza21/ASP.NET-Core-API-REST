Migração de uma aplicação App Web MVC (com persistencia via SQL Server, apresentação, segurança e regras de negocio) para uma
Web API do estilo arquitetural REST, sendo dividida em microserviços.

Trabalho com requests CRUD (HTTP + URI) e responses em JSON, XML ou formatos negociados + Status Code;
Desacoplamento de funções com segurança baseada em tokens via JWT.

Curso Alura "APIs Rest com ASP.NET Core 2.1"


### RUN

Iniciar serviços (Ctrl + F5 no Visual Studio) AuthProvider (porta 5000) e WebAPI (porta 6000);
Iniciar aplicação Web MVC via IIS Explorer;


### Trabalhando com a aplicação

Requisição de token JWT via POST no endpoint 'http://localhost:5000/api/login' com body JSON contendo "login" e "password";
Requisição GET no serviço 'http://localhost:6000' com "Authorization" do tipo 'Bearer Token" contendo o toker em questão;

Exemplo de endpoint do API seria o JSON Data de um livro com Id especifico, como 'http://localhost:6000/api/Livros/1';


### Endpoints

Livros:
- Get /api/Livros
- Get /api/Livros/{id}
- Get /api/Livros/{id}/capa
- Post /api/Livros (+Body)
- Put /api/Livros (+Body)
- Delete /api/Livros/{id}

Listas de leitura:
- Get /api/ListasLeitura
- Get /api/ListasLeitura/{tipo}
