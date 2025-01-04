# Encryption-and-Hashing

Este é um projeto de autenticação de usuários desenvolvido com Node.js, Express, PostgreSQL e bcrypt para criptografia de senhas. A aplicação permite que usuários se registrem e façam login com segurança.

## 🚀 Funcionalidades
- Registro de usuários com hash de senha seguro.
- Login de usuários com validação de credenciais.
- Armazenamento de dados em um banco de dados PostgreSQL.
- Renderização de páginas usando EJS (Embedded JavaScript Templates).

---

## 🛠️ Tecnologias Utilizadas
- [Node.js](https://nodejs.org/) - Plataforma de execução JavaScript.
- [Express](https://expressjs.com/) - Framework web para Node.js.
- [PostgreSQL](https://www.postgresql.org/) - Banco de dados relacional.
- [bcrypt](https://github.com/kelektiv/node.bcrypt.js/) - Biblioteca para hash de senhas.
- [body-parser](https://www.npmjs.com/package/body-parser) - Middleware para manipulação de requisições.
- [EJS](https://ejs.co/) - Template engine para renderização de HTML dinâmico.

---

## ⚙️ Pré-requisitos
- **Node.js** instalado.
- **PostgreSQL** configurado e rodando na máquina local.
- Uma tabela `users` criada no banco de dados `secrets` com a seguinte estrutura:
  ```sql
  CREATE TABLE users (
      id SERIAL PRIMARY KEY,
      email VARCHAR(255) NOT NULL UNIQUE,
      password TEXT NOT NULL
  );

---

## 📂 Estrutura do Projeto

```
📦 root
├── 📂 public          # Arquivos estáticos (CSS, JS, etc.)
├── 📂 views           # Arquivos EJS para renderização de páginas
├── server.js          # Arquivo principal do servidor
├── package.json       # Dependências do projeto
```
---

## 🔒 Segurança
Senhas são armazenadas de forma segura usando hashing com a biblioteca bcrypt.

Utilize variáveis de ambiente para armazenar credenciais sensíveis, como a senha do banco de dados, utilizando pacotes como dotenv.
