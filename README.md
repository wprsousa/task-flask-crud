# Gerenciador de Tarefas com Flask

Este projeto é uma aplicação simples de gerenciamento de tarefas (`CRUD`) usando o framework Flask e testes com pytest.
A aplicação permite criar, visualizar, atualizar e deletar tarefas, e foi desenvolvida para fins de aprendizado.

## Tecnologias Utilizadas

- Python
- Flask
- pytest
- requests (para os testes)

## Estrutura do Projeto

- **app.py**: Contém a aplicação Flask com as rotas para gerenciar tarefas.
- **tests.py**: Arquivo de testes que utiliza pytest para validar as funcionalidades da aplicação.
- **models/task.py**: Classe `Task` usada para representar as tarefas e convertê-las para um formato JSON.

## Endpoints

Abaixo estão os endpoints disponíveis na API:

### 1. Criar Tarefa

- **URL**: `/tasks`
- **Método**: `POST`
- **Corpo da Requisição**:
  ```json
  {
    "title": "Título da tarefa",
    "description": "Descrição da tarefa"
  }

- **Resposta de Sucesso:** 201 Created
    ```json
  {
      "message": "Nova tarefa criada com sucesso!",
      "id": 1
  }

### 2. Listar todas as tarefas

- **URL**: `/tasks`
- **Método**: `GET`
- **Resposta de Sucesso**: 200 OK
  ```json
  {
    "tasks": [...],
    "total_tasks": 1
  }

### 3. Obter detalhes de uma tarefa

- **URL**: `/tasks/<id>`
- **Método**: `GET`
- **Resposta de Sucesso**: 200 OK
  ```json
  {
    "id": 1,
    "title": "Título da tarefa",
    "description: "Descrição da tarefa",
    "completed": false
  }

### 4. Atualizar uma tarefa

- **URL**: `/tasks/<id>`
- **Método**: `PUT`
- **Corpo da Requisição**:
  ```json
  {
    "title": "Título atualizado",
    "description: "Nova descrição",
    "completed": true
  }
- **Resposta de Sucesso:** 200 OK
    ```json
  {
      "message": "Tarefa atualizada com sucesso"
  }

### 5. Deletar uma tarefa

- **URL**: `/tasks/<id>`
- **Método**: `DELETE`
- **Resposta de Sucesso**: 200 OK
  ```json
  {
    "message": "Tarefa deletada com sucesso"
  }

## Como executar a aplicação

1. Clone o repositório:

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
```

2. Crie um ambiente virtual e ative-o:

```bash
python -m venv venv
source venv/bin/activate  # Para Linux/macOS
venv\Scripts\activate  # Para Windows
```

3. Instale as dependências

```bash
pip install -r requirements.txt
```

4. Execute a aplicação

```bash
python app.py
```

5. Acesse a aplicação em http://127.0.0.1:5000

#### Autor:  Wellington Pedro Ranha de Sousa

