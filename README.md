# Aplicação MVC com Integração ao Banco de Dados SQL Server
Esta aplicação utiliza o ASP.NET Core com arquitetura MVC e integra-se a um banco de dados SQL Server. A aplicação permite realizar operações CRUD para manipular registros de contatos no banco de dados. As operações são implementadas usando o Entity Framework Core.

## Tecnologias Utilizadas
- ASP.NET Core MVC
- SQL Server
- Entity Framework Core

## Estrutura do Projeto
- `Controllers/ContatoController.cs: Controlador principal que lida com as operações CRUD para os contatos.
- `Models/Contato.cs: Modelo de dados que representa um contato na aplicação.

## Configuração do Banco de Dados

Para configurar a conexão com o banco de dados SQL Server, forneça a cadeia de conexão no arquivo appsettings.Development.json. A configuração deve ser semelhante à seguinte:

```json
{
  "ConnectionStrings": {
    "ConexaoPadrao": "Server=Nome_do_Server; Initial Catalog=Agenda; Integrated Security=True; Encrypt=False;"
  }
}
```

## Uso da Aplicação
### Rotas da API
- Criar um Contato (POST): POST /Contato/Create - Cria um novo contato no banco de dados.
- Obter um Contato por ID (GET): GET /Contato/Details/{id} - Recupera um contato específico com base no ID fornecido.
- Obter Contatos por Nome (GET): GET /Contato/ObterPorNome - Recupera contatos com base no nome fornecido.
 -Atualizar um Contato por ID (PUT): PUT /Contato/Edit/{id} - Atualiza as informações de um contato existente com base no ID fornecido.
- Deletar um Contato por ID (DELETE): DELETE /Contato/Delete/{id} - Exclui um contato com base no ID fornecido.