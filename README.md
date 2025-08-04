# ✅ MiniTodo API

Uma API REST simples para gerenciamento de tarefas (ToDo), desenvolvida com .NET 6 e SQLite. Este projeto demonstra como utilizar o Entity Framework Core, endpoints minimalistas (Minimal APIs) e validação de dados com ViewModels.

## Funcionalidades

- ✅ Listar todas as tarefas (`GET /v1/todos`)
- ✅ Criar uma nova tarefa (`POST /v1/todos`)
- ✅ Integração com Swagger para testes de endpoint
- ✅ Banco de dados com Entity Framework Core e SQLite

 ## 🛠️ Tecnologias Utilizadas

- [.NET 6](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
- [Entity Framework Core](https://learn.microsoft.com/ef/core/)
- [SQLite](https://www.sqlite.org/)
- [Swagger (Swashbuckle)](https://github.com/domaindrivendev/Swashbuckle.AspNetCore)

MiniTodo/
│
├── Data/
│ └── AppDbContext.cs # Configuração do banco de dados (EF Core)
│
├── Models/
│ └── Todo.cs # Modelo de dados da tarefa
│
├── ViewModels/
│ └── CreateTodoViewModel.cs # ViewModel com validação para criação de tarefas
│
├── Program.cs # Entrypoint com endpoints e configurações

## ⚙️ Como executar o projeto localmente

1. Clone o repositório:
   
   git clone https://github.com/wellington-garcia-silva/Mini-To-Do.git
   cd MiniTodo
   
Restaure os pacotes:
  dotnet restore

Crie o banco de dados:
  dotnet ef migrations add InitialCreate
  dotnet ef database update

Execute o projeto:
  dotnet run

Acesse o Swagger UI:
http://localhost:5000/swagger

🔁 Endpoints da API
🔹 GET /v1/todos
Retorna todas as tarefas cadastradas.

🔹 POST /v1/todos
Cria uma nova tarefa.

Corpo da requisição:
{
  "title": "Ir no Supermecado"
}

Exemplo de resposta
{
  "id": 1,
  "title": "Ir no Supermecado",
  "done": false
}
