# Dojô de Testes Automatizados 🥷

## Objetivo
Nessa dinâmica, vamos conversar sobre o framework cypress e suas funcionalidades básicas. Em seguida, praticaremos alguns dos conceitos demonstrados, automatizando a funcionalidade de cadastro externo de usuários no [Portal do SEST SENAT](https://2-senat-portal-2022.qa.dotgroup.com.br/).

## ⚙️ Introdução
Cypress é uma ferramenta moderna para automação de testes web e de API, conhecida pela simplicidade e rápida curva de aprendizado. Usa as linguagens JavaScript ou TypeScript, o que torna sua implementação versátil e ágil. Conta com uma comunidade ativa, atualizações frequentes e diversas ferramentas para validação. Além disso, oferece um dashboard com métricas, suporte a paralelismo e integração fácil com CI/CD.

### Comparativo entre Frameworks

| Pontos Fortes | Cypress | Robot Framework | Playwright |
|---------------|---------|----------------|------------|
| Documentação | Excelente e bem organizada | Boa, com exemplos práticos | Clara e atualizada |
| Curva de Aprendizado | Rápida para devs JS | Média, sintaxe própria | Moderada |
| Comunidade | Grande e ativa | Estabelecida e madura | Em crescimento |
| Velocidade de Execução | Muito rápida | Média | Rápida |
| Depuração | Excelente UI interativa | Básica | Boa, com Trace Viewer |
| Integração CI/CD | Fácil | Requer configuração | Nativa |

### Metodologia Triple A (AAA)
- **Arrange**: configurações, geração de massa de dados e outras atividades que antecedem o teste;
- **Act**: ações que serão efetuadas durante o teste;
- **Assert**: validações que serão efetuadas ao final do teste para garantir resultados assertivos e precisos;

## 🟡 Configuração do Projeto

### Passos Iniciais
1. Criando um projeto do zero (`npm init` + `npm install cypress --save-dev`);
2. Abrindo a interface do cypress pela primeira vez (`npx cypress open`);
3. Explicando a estrutura de pastas (`cypress/integration`, `cypress/fixtures`, `cypress/support`);
4. Configuração do `cypress.config.js`:
   - **Timeouts**:
     - pageLoadTimeout (60000ms);
     - responseTimeout (5000ms);
     - defaultCommandTimeout (4000ms);
   - **baseUrl**: url que será usada como base em comando como `cy.visit()` e `cy.request()`;
   - **viewports**: configuração das dimensões da tela;
   - **env**: definição de variáveis de ambiente;

## 🔵 Mão na Massa - Hands-on

### Desafios Progressivos

1. **Acesso à página do portal (CT01)**
   - Uso de `cy.visit()`, `cy.get()`, `cy.contains()`;

2. **Acessar tela de cadastro (CT02) e preencher formulário (CT03)**
   - Interação com diferentes tipos de campos;
   - EXTRA: Geração de dados com faker.js;

3. **Validação de campos obrigatórios (CT04)**
   - Teste de mensagens de erro em campos obrigatórios;

4. **Submeter formulário e interceptar requisições**
   - Uso do `cy.intercept()` para validação de requisições;

5. **Versionamento**
   - Envio do código para repositório GitHub;

## 🟣 Melhores Práticas

- Ferramentas de depuração;
- Uso adequado de `cy.wait()`;
- Estruturação de testes (DRY, fixtures);
- Organização do código.

## Contribuição
Sinta-se à vontade para contribuir com este projeto através de Pull Requests ou abrindo Issues para discussão.