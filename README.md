# 🐾 PetCrud

Sistema web para **cadastro e gerenciamento de animais**, desenvolvido utilizando **ASP.NET Core MVC**, **Entity Framework Core** e **SQL Server**.

O projeto permite realizar as principais operações de um CRUD:

* ➕ Cadastrar animais
* 📋 Listar animais cadastrados
* 🔎 Visualizar detalhes
* ✏️ Editar informações
* 🗑️ Excluir animais

---

## 🚀 Tecnologias utilizadas

* **C#**
* **.NET 8**
* **ASP.NET Core MVC**
* **Entity Framework Core 8**
* **SQL Server**
* **Razor**
* **Bootstrap**
* **jQuery**
* **HTML5**
* **CSS3**

---

## 📂 Estrutura do projeto

```text
PetCrud/
├── Controllers/
│   ├── AnimalController.cs
│   └── HomeController.cs
│
├── Models/
│   ├── Animal.cs
│   ├── ErrorViewModel.cs
│   └── PetContext.cs
│
├── Migrations/
│   ├── 20260807173502_CriandoTabela.cs
│   ├── 20260807173502_CriandoTabela.Designer.cs
│   └── PetContextModelSnapshot.cs
│
├── Views/
│   ├── Animal/
│   │   ├── Create.cshtml
│   │   ├── Delete.cshtml
│   │   ├── Details.cshtml
│   │   ├── Edit.cshtml
│   │   └── Index.cshtml
│   │
│   ├── Home/
│   └── Shared/
│
├── wwwroot/
│   ├── css/
│   ├── js/
│   └── lib/
│
├── appsettings.json
├── Program.cs
└── PetCrud.csproj
```

---

## 🐶 Cadastro de animais

Cada animal possui os seguintes dados:

| Campo      | Descrição                     |
| ---------- | ----------------------------- |
| `IdAnimal` | Identificador único do animal |
| `Nome`     | Nome do animal                |
| `Idade`    | Idade do animal               |
| `Raca`     | Raça do animal                |

O modelo principal está representado pela classe `Animal`.

---

## 🗄️ Banco de dados

O projeto utiliza **SQL Server** juntamente com o **Entity Framework Core**.

O contexto do banco é definido na classe:

```text
Models/PetContext.cs
```

A tabela de animais é disponibilizada através de:

```csharp
public DbSet<Animal> Animals { get; set; }
```

### 🔗 Configuração da conexão

A conexão com o banco de dados é configurada no arquivo:

```text
appsettings.json
```

Exemplo:

```json
"ConnectionStrings": {
  "conexao": "Server=SEU_SERVIDOR; Database=DBPetshop; user id=SEU_USUARIO; password=SUA_SENHA; TrustServerCertificate=True"
}
```

> ⚠️ Recomenda-se não compartilhar senhas reais do banco de dados no repositório público. Utilize variáveis de ambiente ou User Secrets em projetos reais.

---

## ⚙️ Como executar o projeto

### 1. Pré-requisitos

Antes de executar o projeto, tenha instalado:

* [.NET 8 SDK](https://dotnet.microsoft.com/)
* SQL Server
* Visual Studio ou Visual Studio Code

---

### 2. Clone o repositório

```bash
https://github.com/GingerProgrammer/PetCrud.git
```

Entre na pasta:

```bash
cd PetCrud
```

---

### 3. Configure o banco de dados

Abra:

```text
PetCrud/appsettings.json
```

e configure a `ConnectionString` de acordo com o seu SQL Server.

---

### 4. Restaure as dependências

```bash
dotnet restore
```

---

### 5. Execute as migrations

Caso o banco ainda não tenha sido criado:

```bash
dotnet ef database update
```

As migrations existentes estão na pasta:

```text
Migrations/
```

---

### 6. Execute o projeto

```bash
dotnet run
```

Depois, acesse o endereço informado pelo terminal, normalmente algo semelhante a:

```text
https://localhost:xxxx
```

ou

```text
http://localhost:xxxx
```

---

## 🔄 Funcionalidades do CRUD

### 📋 Listar

A página inicial de animais apresenta os registros cadastrados no banco de dados.

### ➕ Criar

Permite cadastrar um novo animal informando:

* Nome
* Idade
* Raça

### 🔎 Detalhes

Exibe as informações completas de um animal selecionado.

### ✏️ Editar

Permite alterar os dados de um animal já cadastrado.

### 🗑️ Excluir

Permite remover um animal do banco de dados.

---

## 🏗️ Arquitetura

O projeto segue o padrão **MVC (Model-View-Controller)**:

### Model

Responsável pela representação dos dados e acesso ao banco.

```text
Models/
```

### View

Responsável pela interface apresentada ao usuário.

```text
Views/
```

### Controller

Responsável por receber as requisições e executar as operações do sistema.

```text
Controllers/
```

O principal controller do CRUD é:

```text
AnimalController.cs
```

---

## 📦 Principais pacotes

O projeto utiliza:

```xml
Microsoft.EntityFrameworkCore
Microsoft.EntityFrameworkCore.Design
Microsoft.EntityFrameworkCore.SqlServer
Microsoft.EntityFrameworkCore.Tools
Microsoft.VisualStudio.Web.CodeGeneration.Design
```

---

## 📝 Objetivo

O **PetCrud** foi desenvolvido como um projeto de estudo para praticar conceitos de:

* Desenvolvimento web com ASP.NET Core
* Arquitetura MVC
* C#
* Entity Framework Core
* Operações CRUD
* Integração com SQL Server
* Migrations
* Desenvolvimento de interfaces com Razor e Bootstrap

---

## 👩‍💻 Créditos

**Desenvolvedor**

Mariana Fernandes Souza Santos

---

**Professor**

Wallace Oliveira dos Santos

