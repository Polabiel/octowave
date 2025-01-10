# Octowave - Plataforma de Vendas

**Octowave** é uma solução completa para gerenciamento de vendas, criada para facilitar o controle de comunicações com clientes, registro de transações e organização de dados através de um site intuitivo e poderoso.

---

## Índice

1. [Recursos Principais](#recursos-principais)
2. [Tecnologias Utilizadas](#tecnologias-utilizadas)
3. [Configuração do Ambiente](#configuração-do-ambiente)
4. [Execução da Plataforma](#execução-da-plataforma)
5. [Endpoints da API](#endpoints-da-api)
6. [Contribuição](#contribuição)
7. [Licença](#licença)

---

## Recursos Principais

- **Gerenciamento Centralizado:** Controle total de vendas, clientes e comunicações em um único lugar.
- **Integração com WhatsApp:** Utiliza a biblioteca Baileys API para interagir diretamente com os clientes por mensagens.
- **Banco de Dados Robustos:** Registre vendas e organize as informações de maneira eficiente.
- **Execução em Containers:** Graças ao Docker, o ambiente é facilmente configurável e isolado.
- **Interface Intuitiva:** Plataforma web simples e fácil de usar.

---

## Tecnologias Utilizadas

- **Frontend:** [Next.js 15](https://nextjs.org/) com [Tailwind CSS](https://tailwindcss.com/)
- **Backend:** API REST utilizando Express
- **Banco de Dados:** Prisma como ORM, com suporte a Postgres e MySQL
- **Mensageria:** [Baileys API](https://github.com/adiwajshing/Baileys) para integração com o WhatsApp
- **Containerização:** [Docker](https://www.docker.com/)

---

## Configuração do Ambiente

### Requisitos:

- [Docker](https://www.docker.com/) instalado
- Node.js (v16 ou superior)
- Gerenciador de pacotes: [npm](https://www.npmjs.com/) ou [yarn](https://yarnpkg.com/)

### Configuração Inicial:

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/octowave.git
   cd octowave
   ```

2. Configure as variáveis de ambiente:
   Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:
   ```env
   DATABASE_URL=postgresql://usuario:senha@localhost:5432/octowave
   WHATSAPP_SESSION=seu-token-aqui
   ```

3. Inicie os containers Docker:
   ```bash
   docker-compose up -d
   ```

---

## Execução da Plataforma

### Backend:
1. Instale as dependências:
   ```bash
   npm install
   ```
2. Inicie o servidor:
   ```bash
   npm start
   ```

### Frontend:
1. Navegue até a pasta do frontend:
   ```bash
   cd frontend
   ```
2. Instale as dependências:
   ```bash
   npm install
   ```
3. Inicie o servidor:
   ```bash
   npm start
   ```

---

## Endpoints da API

### Autenticação
- **POST /api/auth/login**
  - Parâmetros: `{ email, password }`
  - Retorna: Token de autenticação

### Vendas
- **GET /api/sales**
  - Retorna: Lista de vendas registradas

- **POST /api/sales**
  - Parâmetros: `{ clientId, products, total }`
  - Retorna: Dados da venda criada

### Mensagens
- **POST /api/messages/send**
  - Parâmetros: `{ clientId, message }`
  - Retorna: Confirmação de envio

---

## Contribuição

Contribuições são bem-vindas! Siga os passos abaixo:

1. Fork o repositório.
2. Crie uma branch:
   ```bash
   git checkout -b sua-branch
   ```
3. Faça suas modificações e commit:
   ```bash
   git commit -m "Adiciona novo recurso"
   ```
4. Envie as alterações:
   ```bash
   git push origin sua-branch
   ```
5. Abra um Pull Request.

---

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
