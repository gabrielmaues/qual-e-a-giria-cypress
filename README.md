# Qual é a Gíria – Testes Automatizados

Automação de testes end-to-end para a aplicação **Qual é a Gíria**, utilizando o framework Cypress.

## 📌 Objetivo

Este projeto tem como objetivo validar funcionalidades principais da aplicação, garantindo que fluxos críticos funcionem corretamente através de testes automatizados.

Entre os cenários testados estão:

* Login de usuário
* Inserção de novas gírias
* Validação do significado cadastrado
* Interação com formulários e elementos da interface

## 🚀 Tecnologias utilizadas

* JavaScript
* Cypress
* Node.js
* Page Object Pattern

## 📂 Estrutura do projeto

```
cypress/
 ├─ e2e/           # Testes end-to-end
 ├─ fixtures/      # Dados de teste (JSON)
 ├─ pages/         # Page Objects
 ├─ support/       # Comandos customizados e configurações

cypress.config.js  # Configuração do Cypress
package.json       # Dependências do projeto
```

## ⚙️ Instalação

Clone o repositório:

```
git clone https://github.com/gabrielmaues/qual-e-a-giria-cypress.git
```

Entre na pasta do projeto:

```
cd qual-e-a-giria-cypress
```

Instale as dependências:

```
npm install
```

## ▶️ Executar os testes

Abrir interface do Cypress:

```
npx cypress open
```

Executar testes no modo headless:

```
npx cypress run
```

## 🧪 Padrões utilizados

O projeto utiliza o padrão **Page Object**, que separa:

* **Testes** → Cenários e validações
* **Pages** → Interações com a interface

Isso facilita:

* manutenção
* reutilização de código
* legibilidade dos testes

## ⚡ Custom Commands

Foram criados **comandos customizados** para reutilizar ações comuns e evitar repetição de código nos testes.

Esses comandos ficam no diretório:

```
cypress/support/commands.js
```

### Exemplos de comandos utilizados

**Inicializar aplicação**

```
cy.start()
```

Responsável por abrir a aplicação e preparar o ambiente inicial para os testes.

**Realizar login**

```
cy.submitLogin(email, password)
```

Executa o fluxo de login automaticamente, preenchendo os campos e enviando o formulário.

### Vantagens dos Custom Commands

* Redução de código duplicado
* Testes mais limpos e legíveis
* Centralização da lógica reutilizável
* Facilidade de manutenção

## 📊 Boas práticas aplicadas

* Uso de **fixtures** para dados de teste
* **Custom Commands** para reutilização de ações
* Separação entre **testes e interações com a página**
* Seletores mais estáveis para evitar testes frágeis
* Estrutura escalável para novos cenários
