

# Backend - Teste Técnico Flutter + Node.js

Este é um backend simples em Node.js (Express.js) criado para servir como intermediário entre um app Flutter 
e uma API pública de dados (JSONPlaceholder).

---

## Como rodar o backend

1. Clone ou baixe este repositório.
2. Abra o terminal (Prompt de Comando ou PowerShell) e navegue até a pasta do backend:

   ```
   cd caminho\para\backend
   ```
3. Instale as dependências:

   ```
   npm install
   ```
4. Inicie o servidor:

   ```
   npm start
   ```

   O servidor irá rodar por padrão em [http://localhost:3000](http://localhost:3000).

---

## Endpoint disponível

* **GET `/api/data`**
  Retorna a lista de usuários obtida da API pública JSONPlaceholder.

  Exemplo:

  ```
  http://localhost:3000/api/data
  ```

---

## Estrutura do projeto

* `index.js`: Código principal do servidor Express
* `package.json`: Dependências e scripts
* `README.md`: Este arquivo

---

## Observações

* O backend está preparado para ser consumido localmente por um app Flutter (ou qualquer frontend).
* Para uso em emulador Android, configure a URL no Flutter como `http://10.0.2.2:3000/api/data`.
* Pode ser facilmente containerizado via Docker para rodar em produção ou na nuvem.

---
