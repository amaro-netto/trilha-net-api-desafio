# DIO - Trilha .NET - API e Entity Framework
# Sistema Agendador de Tarefas

![Badge .NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Badge C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)

## 📋 Descrição do Projeto

Este projeto foi desenvolvido como parte do desafio final do módulo de API e Entity Framework da trilha .NET da **Digital Innovation One (DIO)**.

O objetivo foi construir um sistema gerenciador de tarefas onde é possível cadastrar, listar, atualizar e deletar tarefas. A persistência dos dados é feita através do **Entity Framework Core**.

Embora o desafio original sugerisse o uso do SQL Server, este projeto foi configurado para utilizar **SQLite**, permitindo que ele seja executado facilmente em qualquer ambiente (incluindo GitHub Codespaces) sem a necessidade de instalação de um servidor de banco de dados complexo.

## ⚙️ Funcionalidades

- **CRUD Completo**:
  - Criar nova tarefa.
  - Listar todas as tarefas.
  - Buscar tarefa por ID.
  - Atualizar tarefa existente.
  - Deletar tarefa.
- **Filtros Personalizados**:
  - Buscar tarefas por **Título**.
  - Buscar tarefas por **Data**.
  - Buscar tarefas por **Status** (Pendente/Finalizado).

## 🛠️ Tecnologias Utilizadas

- **.NET 6**
- **C#**
- **Entity Framework Core**
- **SQLite** (Banco de dados relacional portátil)
- **Swagger** (Documentação da API)

## 🚀 Como Executar o Projeto

Para rodar este projeto na sua máquina local ou no GitHub Codespaces, siga os passos abaixo:

### Pré-requisitos
- .NET SDK 6.0 instalado.

### Passos

1. **Clone o repositório**:
   ```bash
   git clone [https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git](https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git)
   ```

2. **Entre na pasta do projeto**:
   ```bash
   cd trilha-net-api-desafio
   ```

3. **Restaure as dependências**:
   ```bash
   dotnet restore
   ```

4. **Atualize o banco de dados (Aplicar Migrations)**:
   Como o projeto usa SQLite, este comando criará o arquivo do banco localmente.
   ```bash
   dotnet ef database update
   ```

5. **Execute o projeto**:
   ```bash
   dotnet run
   ```

6. **Acesse a documentação (Swagger)**:
   Abra o navegador e acesse a porta local indicada no terminal (geralmente `5000` ou `7000`) com o caminho `/swagger`.
   Exemplo: `http://localhost:5181/swagger`

## 🧪 Exemplo de JSON para Teste

Ao criar uma tarefa (POST), utilize o seguinte formato:

```json
{
  "titulo": "Finalizar desafio da DIO",
  "descricao": "Implementar os métodos do Controller e configurar o EF",
  "data": "2024-12-30T10:00:00",
  "status": "Pendente"
}
```

## 📝 Estrutura do Projeto

- **Controllers**: Contém a lógica dos endpoints da API (`TarefaController`).
- **Models**: Contém as classes que representam as tabelas do banco (`Tarefa`) e enums (`EnumStatusTarefa`).
- **Context**: Configuração do contexto do banco de dados (`OrganizadorContext`).
