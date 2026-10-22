# Projeto Carros

Aplicação web para cadastrar, consultar e gerenciar carros, com cadastro de usuários, autenticação e upload de fotos. O projeto reúne práticas de desenvolvimento backend com Python e Django em um contexto de estudo.

## Origem

Este projeto foi desenvolvido durante um curso da PycodeBR, acompanhando a construção de uma aplicação Django para gerenciamento de carros. A estrutura inicial e os exemplos das aulas serviram como base para o aprendizado.

## Minha participação

Além de reproduzir os exemplos das aulas, fiz adaptações nas views e nos modelos (`models.py`), desenvolvi alguns scripts por conta própria e acrescentei validações.

## Funcionalidades

- Cadastro de usuários, login e logout.
- Cadastro, listagem e busca de carros.
- Visualização de detalhes, edição e exclusão de carros.
- Upload de fotos dos veículos.
- Validações de formulário para os dados de cadastro.

## Tecnologias e organização

- Python e Django.
- SQLite para o banco de dados de desenvolvimento.
- Templates Django para a interface.
- Pillow para o suporte ao upload de imagens.
- `python-dotenv` para carregar a configuração local a partir do arquivo `.env`.

| Diretório | Responsabilidade |
|---|---|
| `app/` | Configuração do projeto, rotas e template base. |
| `cars/` | Modelos de carros e marcas, formulários, views e templates dos veículos. |
| `accounts/` | Cadastro de usuários e autenticação. |

## Execução local

Pré-requisitos: Python compatível com as dependências de `requirements.txt`, Git e um ambiente virtual.

Os comandos abaixo usam PowerShell no Windows:

```powershell
git clone https://github.com/Jklimaitis/Projeto_Carros.git
cd Projeto_Carros
python -m venv venv
.\venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
Copy-Item .env.example .env
```

Antes de iniciar a aplicação, configure `DJANGO_SECRET_KEY` no arquivo `.env` com um valor local próprio. Não versione esse arquivo.

```powershell
python manage.py migrate
python manage.py runserver
```

Com o servidor de desenvolvimento iniciado, a listagem de carros fica em `http://127.0.0.1:8000/cars/`.

## Limitações

- O projeto tem finalidade de estudo e utiliza configuração de desenvolvimento; não é apresentado como uma aplicação pronta para produção.
- Os arquivos `cars/tests.py` e `accounts/tests.py` ainda contêm apenas o esqueleto inicial de testes do Django, sem casos implementados.
- As adaptações pessoais não estão discriminadas por função ou commit neste README.
