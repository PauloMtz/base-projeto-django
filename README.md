# Projeto Base Django

Repositório com a estrutura inicial de um projeto criado com Django, com base em vídeo complementar de treinamento da plataforma Udemy, disponível em: https://www.youtube.com/watch?v=tr3RkGkbEU4

## Como criar o ambiente virtual

### Windows

Crie o ambiente virtual na raiz do projeto:

```powershell
python -m venv .venv
```

Ative o ambiente virtual:

```powershell
.venv\Scripts\Activate.ps1
.venv\Scripts\activate
```

### Linux

Crie o ambiente virtual na raiz do projeto:

```bash
python3 -m venv .venv
```

Ative o ambiente virtual:

```bash
source .venv/bin/activate
```

## Como instalar as dependencias

Com o ambiente virtual ativo, instale os pacotes principais usados neste inicio de projeto:

```bash
pip install Django pillow
```

## Como criar um projeto com Django

Depois de ativar o ambiente virtual e instalar as dependencias, crie o projeto com o comando abaixo:

```bash
django-admin startproject core .
```

Esse comando cria a configuracao principal do Django na pasta `core` e o arquivo `manage.py` na raiz do projeto.

## Dependencias instaladas ate o momento

As dependencias encontradas atualmente no ambiente virtual do projeto sao:

- `Django==6.0.7`: framework principal da aplicacao.
- `pillow==12.3.0`: biblioteca para processamento de imagens em Python.
- `asgiref==3.12.1`: suporte a interface ASGI usada pelo Django.
- `sqlparse==0.5.5`: utilitario usado pelo Django para formatacao e analise de comandos SQL.
- `tzdata==2026.3`: base de dados de fuso horario usada pelo Python e pelo Django quando necessario.

## Para que serve o Pillow

O Pillow e a biblioteca mais usada em Python para abrir, validar, converter, redimensionar e salvar imagens. Em projetos Django, ele normalmente e utilizado quando a aplicacao trabalha com upload de imagens, campos `ImageField` e manipulacao de arquivos como fotos de usuarios, produtos ou banners.

## Iniciar o servidor de desenvolvimento:

```bash
python manage.py runserver
```

Depois de iniciar o servidor com esse comando, a aplicacao ficara disponivel em:

```text
http://127.0.0.1:8000/
```

Se preferir, voce tambem pode acessar pela URL equivalente:

```text
http://localhost:8000/
```
