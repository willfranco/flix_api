# 🎬 API RESTful para Gerenciamento de Filmes, Atores, Gêneros e Avaliações

Este projeto é uma API RESTful desenvolvida com Django Rest Framework (DRF) para gerenciar informações sobre filmes, atores, gêneros e avaliações. A autenticação é baseada em JWT, e há um sistema de permissões para diferentes níveis de usuários.

## 🚀 Tecnologias Utilizadas
- Python
- Django
- Django Rest Framework
- PostgreSQL (ou SQLite para desenvolvimento)
- Simple JWT para autenticação

## 📌 Funcionalidades
A API fornece um CRUD completo para as seguintes entidades:
- **Movies (Filmes)**: Criar, listar, atualizar e excluir filmes.
- **Actors (Atores)**: Criar, listar, atualizar e excluir atores.
- **Genres (Gêneros)**: Criar, listar, atualizar e excluir gêneros.
- **Reviews (Avaliações)**: Criar, listar, atualizar e excluir avaliações.

## 🔑 Autenticação e Permissões
- Autenticação via JWT (JSON Web Token).
- Apenas usuários autenticados podem acessar determinados endpoints.
- Diferentes permissões de acesso para administradores e usuários comuns.

## 📦 Instalação e Configuração
### 1. Clone o repositório:
```bash
$ git clone https://github.com/seu-usuario/nome-do-repositorio.git
$ cd nome-do-repositorio
```

### 2. Crie um ambiente virtual e ative-o:
```bash
$ python -m venv venv
$ source venv/bin/activate  # Para Linux/Mac
$ venv\Scripts\activate  # Para Windows
```

### 3. Instale as dependências:
```bash
$ pip install -r requirements.txt
```

### 4. Configure o banco de dados e execute as migrações:
```bash
$ python manage.py migrate
```

### 5. Crie um superusuário:
```bash
$ python manage.py createsuperuser
```

### 6. Execute o servidor:
```bash
$ python manage.py runserver
```

A API estará disponível em `http://127.0.0.1:8000/`

## 📖 Endpoints Principais
### Autenticação
- `POST authentication/token/` → Gera um token JWT.
- `POST authentication/token/refresh/` → Atualiza o token JWT.
- `POST authentication/token/verify/` → Verifica o token JWT.

### Filmes
- `GET /api/v1/movies/` → Lista todos os filmes.
- `POST /api/v1//movies/` → Cria um novo filme (requer autenticação).
- `GET /api/v1//movies/{id}/` → Obtém detalhes de um filme.
- `PUT /api/v1//movies/{id}/` → Atualiza um filme (requer autenticação).
- `DELETE /api/v1//movies/{id}/` → Exclui um filme (somente admin).

### Atores
- `GET /api/v1//actors/` → Lista todos os atores.
- `POST /api/v1/ /actors/` → Cria um novo ator (requer autenticação).
- `GET /api/v1/ /actors/{id}/` → Obtém detalhes de um ator.
- `PUT /api/v1/ /actors/{id}/` → Atualiza um ator (requer autenticação).
- `DELETE /api/v1/ /actors/{id}/` → Exclui um ator (somente admin).

### Gêneros
- `GET /api/v1/ /genres/` → Lista todos os gêneros.
- `POST /api/v1/ /genres/` → Cria um novo gênero (requer autenticação).
- `GET /api/v1/ /genres/{id}/` → Obtém detalhes de um gênero.
- `PUT /api/v1/ /genres/{id}/` → Atualiza um gênero (requer autenticação).
- `DELETE /api/v1/ /genres/{id}/` → Exclui um gênero (somente admin).

### Avaliações
- `GET /api/v1/ /reviews/` → Lista todas as avaliações.
- `POST /api/v1/ /reviews/` → Cria uma nova avaliação (requer autenticação).
- `GET /api/v1/ /reviews/{id}/` → Obtém detalhes de uma avaliação.
- `PUT /api/v1/ /reviews/{id}/` → Atualiza uma avaliação (requer autenticação).
- `DELETE /api/v1/ /reviews/{id}/` → Exclui uma avaliação (somente admin).


---

Desenvolvido por [William Amaral Franco](https://github.com/willfranco) 🚀

