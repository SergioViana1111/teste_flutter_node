

# Teste Técnico – Flutter + Node.js

Este projeto é uma solução para o teste técnico, onde o objetivo é criar um backend em Node.js (Express.js) que consome uma API pública(JSONPlaceholder) e expõe os dados para serem utilizados em um aplicativo Flutter. O app Flutter consome esses dados via HTTP e exibe em uma interface simples, com botão para recarregar os dados.

---

## 📁 Estrutura do Projeto

```

/
├── backend/           # Backend Node.js (Express)
│   ├── index.js
│   ├── package.json
│   └── Dockerfile
│
└── flutter\_app/       # App Flutter (frontend)
├── lib/
│   └── main.dart
├── pubspec.yaml

````

---

## 🚀 Como Rodar o Projeto

### Pré-requisitos

- Node.js (v18 ou superior)
- NPM (Node Package Manager)
- Flutter SDK (3.x)
- (Opcional) Docker Desktop

---

### 1. Rodando o Backend (Node.js)

```sh
cd backend
npm install
npm start
````

* O backend ficará disponível em:
  `http://localhost:3000/api/data`

#### Docker (opcional):

```sh
cd backend
docker build -t backend-flutter-teste .
docker run -p 3000:3000 backend-flutter-teste
```

---

### 2. Rodando o App Flutter

```sh
cd flutter_app
flutter pub get
flutter run -d chrome
```

* O app por padrão está configurado para buscar dados em `http://localhost:3000/api/data`.
* Se rodar no **emulador Android**, use `http://10.0.2.2:3000/api/data` no código.

---

## 🧩 Tecnologias Utilizadas

* **Backend:** Node.js, Express.js, Axios, CORS
* **Frontend:** Flutter, http package
* **API Pública:** JSONPlaceholder ([https://jsonplaceholder.typicode.com/users](https://jsonplaceholder.typicode.com/users))
* **Docker:** (para containerizar o backend, opcional)

---

## 🔗 Endpoints Backend

* **GET /api/data**
  Retorna um array de usuários da API pública JSONPlaceholder.

---

## 💻 Funcionalidades do App Flutter

* Exibe uma lista de usuários vindos da API.
* Botão flutuante para recarregar os dados da API.
* Loading e tratamento básico de erro de conexão.

---

## 📦 Estrutura Recomendada de Pastas

```
/backend
  - index.js
  - package.json
  - Dockerfile

/flutter_app
  - lib/main.dart
  - pubspec.yaml
```

---

## 👨‍💻 Como clonar e rodar rapidamente

```sh
git clone https://github.com/SEUUSUARIO/SEUREPOSITORIO.git
cd backend
npm install
npm start

# Abra outro terminal
cd flutter_app
flutter pub get
flutter run -d chrome
```

---

## 📝 Observações

* Testado em Windows 10 e Ubuntu.
* Para rodar tudo em Docker, só o backend precisa ser containerizado.
* Sugestão: rodar backend primeiro, depois o Flutter.
* Caso rode em nuvem ou com IP diferente, lembre de ajustar a URL do backend no app Flutter.

---

## 📄 Licença

Este projeto é open-source, use como quiser.

