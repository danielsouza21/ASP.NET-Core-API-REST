Migração de uma aplicação App Web MVC (aplicação monolítica com persistencia via SQL Server, apresentação, segurança e regras de negocio) para uma Web API do estilo arquitetural REST, sendo dividida em microserviços e seguindo o padrão 'clean'.

- Desacoplamento do App Web MVC (agora este responsável apenas pela apresentação / views), sendo transferido a responsabilidade de persistência e regras de negócio para o endpoint do servidor de web API, e alocando a segurança para o projeto de AuthenticationProvider (servidor secundário para geração dos tokens de acesso);

- Trabalho com requests CRUD (HTTP + URI) e responses em JSON, XML ou formatos negociados + Status Code, consumindo assim a API via IHttpClientFactory;

- Funções de segurança baseada em tokens JWT e cookies;

- Versionamento de aplicação;

- Trabalho com grandes quantidades de dados via paginação, ordenação e filtro via query utilizando o pacote do Linq DynamicCore;

- Padronização e uniformização de erros da API;

- Documentação da API via swagger [localhost:6001/swagger/index.html] através do pacote Swashbuckle do AspNetCore, seguindo o padrão Open API.

---

> Curso Alura "APIs Rest com ASP.NET Core 2.1"

---

### RUN

Iniciar serviços (Ctrl + F5 no Visual Studio) AuthProvider (porta 5000) e WebAPI (porta 6001);

Iniciar aplicação Web MVC via IIS Explorer;

> Acessar documentação via swagger (necessário request de BearerToken de autorização JWT);
