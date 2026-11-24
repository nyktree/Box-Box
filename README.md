# Box Box

Sistema web para gestão de oficina mecânica, desenvolvido com Python, Django, SQLite, HTML, CSS e JavaScript.

## Recursos

- Usuários com perfis de administrador, atendente e mecânico.
- Cadastro de clientes e veículos.
- Ordens de serviço, avarias, diagnósticos e peças.
- Histórico de status.
- Relatórios em CSV e PDF.
- Arquivamento e restauração pela lixeira.

## Requisitos

- Python 3.12 ou superior.
- Windows, Linux ou macOS.

## Instalação manual

```bash
python -m venv .venv
```

Ative o ambiente virtual:

```powershell
# Windows
.venv\Scripts\activate
```

```bash
# Linux ou macOS
source .venv/bin/activate
```

Instale e prepare o projeto:

```bash
python -m pip install -r requirements.txt
python manage.py migrate
python manage.py seed_demo
python manage.py runserver
```

Acesse http://127.0.0.1:8000/.

No Windows, também é possível executar `run-boxbox.bat`.

## Usuários demonstrativos

| Perfil | Usuário | Senha |
|---|---|---|
| Administrador | `admin` | `boxbox123` |
| Atendente | `atendente` | `boxbox123` |
| Mecânico | `mecanico` | `boxbox123` |

Os usuários são criados pelo comando `python manage.py seed_demo`.

## Configuração

O projeto funciona localmente sem arquivo `.env`. Para outras instalações, use `.env.example` como referência e configure as variáveis no ambiente.

O banco `db.sqlite3` é criado por `python manage.py migrate` e não deve ser enviado ao repositório.