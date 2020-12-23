Migração de uma aplicação App Web MVC (com persistencia via SQL Server, apresentação, segurança e regras de negocio) para uma
Web API do estilo arquitetural REST, sendo dividida em microserviços e seguindo o padrão 'clean'.

- Desacoplamento do App Web MVC (agora este responsável apenas pela apresentação / views), sendo transferido a responsabilidade de persistência e regras de negócio para o endpoint do servidor de web API, e alocando a segurança para o projeto de AuthenticationProvider (servidor secundário para geração dos tokens de acesso); 

- Trabalho com requests CRUD (HTTP + URI) e responses em JSON, XML ou formatos negociados + Status Code, consumindo assim a API via IHttpClientFactory;

- Funções de segurança baseada em tokens JWT e cookies.

---

> Curso Alura "APIs Rest com ASP.NET Core 2.1"

---

### RUN

Iniciar serviços (Ctrl + F5 no Visual Studio) AuthProvider (porta 5000) e WebAPI (porta 6000);

Iniciar aplicação Web MVC via IIS Explorer;

### Endpoints da API

> Necessário token de acesso, requisitado via requisição POST na URI [http://localhost:5000/api/login] com body JSON contendo 'login' e 'password';

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
