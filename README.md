# Sistema Web - Cadastro de Alunos

Projeto full-stack de **Cadastro de Alunos** desenvolvido com **HTML, CSS, JavaScript (Front-end)**, **Python + Flask (API REST)** e **MySQL (Banco de Dados)**.

Neste desafio (*Nova demanda no sistema web*), o sistema foi expandido para contemplar os novos campos de **Telefone** e **Data de Nascimento** tanto no formulário e listagem web quanto nos endpoints CRUD da API e na tabela do banco de dados.

## Estrutura do Projeto

- `index.html` — Interface web com formulário de cadastro/edição e tabela de alunos.
- `style.css` — Estilização responsiva da página, formulário e tabela.
- `script.js` — Consumo da API REST (`GET`, `POST`, `PUT`, `DELETE`) via `fetch`.
- `app.py` — API REST em Flask conectada ao MySQL (`escola_db`).
- `database.sql` — Script SQL para criação do banco `escola_db` e da tabela `alunos`.
- `estrutura_tabela_mysql.txt` — Estrutura da tabela `alunos` no MySQL (`DESCRIBE alunos`).
- `requirements.txt` — Dependências Python do servidor Flask.

## Pré-requisitos

- Python 3.8+
- Servidor MySQL

## Como executar

1. **Banco de Dados (MySQL):**
   Execute o script `database.sql` no seu MySQL para criar o banco `escola_db` e a tabela `alunos`:
   ```bash
   mysql -u root -p < database.sql
   ```

2. **Back-end (API Flask):**
   Instale as dependências e inicie o servidor:
   ```bash
   pip install -r requirements.txt
   python app.py
   ```
   A API ficará disponível na porta `5000`.

3. **Front-end:**
   Abra o arquivo `index.html` no navegador (ou sirva-o via servidor HTTP/Apache). Certifique-se de que a constante `api` no topo de `script.js` aponta para o endereço onde o back-end está rodando (por exemplo, `http://localhost:5000`).
