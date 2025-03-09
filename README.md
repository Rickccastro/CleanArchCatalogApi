# 🚀 API de Cadastro de Categorias e Produtos

## 📌 Visão Geral
Esta API foi desenvolvida para o estudo dos princípios da **Clean Architecture**, garantindo separação de responsabilidades, manutenção facilitada e expansibilidade do projeto. 🛠️

## 🏛️ Clean Architecture
A **Clean Architecture**, proposta por Robert C. Martin (Uncle Bob), tem como objetivo principal organizar o código de forma que os detalhes (frameworks, banco de dados, interface gráfica, etc.) sejam menos acoplados às regras de negócio. 

### 🔍 Camadas do Projeto
A arquitetura está dividida nas seguintes camadas:

1. **Domain (Domínio) 📜**
   - Contém as entidades principais da aplicação.
   - Define interfaces e regras de negócio.
   - Independe de detalhes externos (banco de dados, frameworks, etc.).

2. **Application (Aplicação) 🏗️**
   - Contém os casos de uso da aplicação.
   - Faz a interação entre a camada de Domínio e a camada de Infraestrutura.
   - Utiliza padrões como **CQRS** e **MediatR** para separação clara de responsabilidades.

3. **Infrastructure (Infraestrutura) 🔧**
   - Implementação dos repositórios e integração com o banco de dados.
   - Fornece serviços como autenticação, envio de e-mails e comunicação com APIs externas.

4. **Presentation (Apresentação) 🎨**
   - Contém os controladores da API.
   - Define endpoints e intermedia as requisições do cliente.
   - Utiliza **Swagger** para documentação interativa.
   
<img src="https://github.com/user-attachments/assets/1a0be2e8-6712-45fb-a97c-ad9ccaed00a6" width="500" />

## 🧐 Quando utilizar esta arquitetura?
- **Projetos de Médio a Grande Porte 💼**: A Clean Architecture é ideal para sistemas mais complexos, que exigem manutenção a longo prazo e uma base de código mais robusta.
- **Sistemas que exigem escalabilidade 📈**: Quando há a necessidade de expandir a aplicação de forma que cada camada seja facilmente modificada ou substituída sem grandes impactos nas demais.
- **Aplicações que envolvem múltiplos frameworks ou tecnologias 🔧**: Se você precisar trocar tecnologias ao longo do tempo (ex: trocar um ORM ou banco de dados), essa arquitetura facilita essas mudanças.

## ✨ Características
- **Independente de Frameworks 📚**: A arquitetura separa as camadas, permitindo que você troque frameworks sem impactar as regras de negócio.
- **Testável 🧪**: Com a separação das responsabilidades, as camadas podem ser testadas individualmente, melhorando a qualidade do código.
- **Independente da Camada de Apresentação (UI) 🎮**: A lógica de negócios e a interface de usuário são desacopladas, facilitando mudanças no front-end sem afetar o back-end.
- **Independente do Banco de Dados 🗃️**: A camada de domínio não depende de detalhes do banco de dados, permitindo a troca entre PostgreSQL, MySQL ou qualquer outro banco com pouca alteração.
- **Independente de Fatores Externos 🌍**: A aplicação se mantém flexível a mudanças, como autenticação, envio de e-mails e integrações externas.


### ✅ Vantagens & ⚠️ Desvantagens

| **Vantagens** 🔝  | **Desvantagens** ⚙️ |
|------------------|---------------------|
| **Escalabilidade e Manutenção**: A separação clara de responsabilidades facilita a manutenção do código à medida que o projeto cresce, tornando-o mais escalável. | **Curva de Aprendizado**: A implementação de uma arquitetura mais complexa pode exigir um tempo maior de aprendizado e adaptação. |
| **Facilidade de Testes**: A arquitetura permite o uso de testes unitários e de integração, tornando a aplicação mais robusta. | **Complexidade Inicial**: Em projetos menores, pode parecer excessiva, já que o setup inicial é mais trabalhado do que uma arquitetura mais simples. |
| **Flexibilidade de Mudanças**: Mudanças no banco de dados, frameworks ou UI podem ser feitas de forma isolada sem impacto em outras partes do sistema. | |



## 🛠️ Tecnologias Utilizadas
- **Linguagem:** C# 💻
- **Framework:** .NET 🌐
- **Banco de Dados:** PostgreSQL/MySQL 🗄️
- **ORM:** Entity Framework Core 🔗
- **Padrão Arquitetural:** Clean Architecture 🏛️

## 🔗 Endpoints
A API disponibiliza os seguintes endpoints:

### 📂 **Categorias**
- `POST /api/Categorias` - Cadastrar uma nova categoria. ➕
- `GET /api/Categorias` - Listar todas as categorias. 📋
- `GET /api/Categorias/{id}` - Obter uma categoria por ID. 🔍
- `PUT /api/Categorias/{id}` - Atualizar uma categoria. ✏️
- `DELETE /api/Categorias/{id}` - Remover uma categoria. ❌

### 📦 **Produtos**
- `POST /api/Produtos` - Cadastrar um novo produto. ➕
- `GET /api/Produtos` - Listar todos os produtos. 📋
- `GET /api/Produtos/{id}` - Obter um produto por ID. 🔍
- `PUT /api/Produtos/{id}` - Atualizar um produto. ✏️
- `DELETE /api/Produtos/{id}` - Remover um produto. ❌

## ⚙️ Instalação e Execução
1. Clone o repositório:
   ```sh
   git clone https://github.com/Rickccastro/CleanArchCatalogApi.git
   ```
2. Navegue até a pasta do projeto:
   ```sh
   cd CleanArchCatalogApi/Catalogo.API
   ```
3. Configure a string de conexão no `appsettings.json`. 🛠️
4. Execute as migrações do banco de dados:
   ```sh
   dotnet ef database update
   ```
5. Inicie a aplicação:
   ```sh
   dotnet run
   ```
## 📚 Referências
- [Macoratti.net](https://www.macoratti.net/)

