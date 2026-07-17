# Projeto Base Django

Repositório com a estrutura inicial de um projeto criado com Django, com base em vídeo complementar de treinamento da plataforma Udemy, disponível em: https://www.youtube.com/watch?v=tr3RkGkbEU4 (com adaptações de aula da Treinaweb - curso de Apis com Django)

## Como criar o ambiente virtual

### Windows

Crie o ambiente virtual na raiz do projeto:

```powershell
python -m venv .venv
```

Ative o ambiente virtual:

```powershell
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
pip install Django pillow python-decouple dj-database-url mysqlclient black
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
- `python-decouple==3.8`: leitura de variaveis de ambiente a partir do arquivo `.env`, ajudando a separar configuracoes sensiveis do codigo.
- `dj-database-url==3.1.2`: converte a string de conexao do banco em configuracao compativel com o Django.
- `mysqlclient==2.2.8`: driver usado pelo Django para conectar em bancos MySQL.
- `black==26.5.1`: formatador automatico de codigo Python, usado para padronizar o estilo do projeto.
- `asgiref==3.12.1`: suporte a interface ASGI usada pelo Django.
- `sqlparse==0.5.5`: utilitario usado pelo Django para formatacao e analise de comandos SQL.
- `tzdata==2026.3`: base de dados de fuso horario usada pelo Python e pelo Django quando necessario.
- `click==8.4.2`: dependencia de linha de comando usada internamente pelo Black.
- `colorama==0.4.6`: melhora a exibicao de saida colorida no terminal, principalmente no Windows.
- `mypy_extensions==1.1.0`: pacote auxiliar usado por ferramentas de desenvolvimento como o Black.
- `packaging==26.2`: ajuda no tratamento de versoes e metadados de pacotes Python.
- `pathspec==1.1.1`: usado pelo Black para respeitar padroes de arquivos e diretorios.
- `platformdirs==4.10.0`: localiza diretorios padrao do sistema operacional para cache e configuracoes.
- `pytokens==0.4.1`: dependencia interna usada pelo Black durante a formatacao do codigo.

## Para que serve o Pillow

O Pillow e a biblioteca mais usada em Python para abrir, validar, converter, redimensionar e salvar imagens. Em projetos Django, ele normalmente e utilizado quando a aplicacao trabalha com upload de imagens, campos `ImageField` e manipulacao de arquivos como fotos de usuarios, produtos ou banners.

## Como configurar o formatador Black

O Black e o formatador de codigo Python adotado neste projeto. Ele organiza automaticamente a identacao, espacos, quebras de linha e outros detalhes de estilo para manter o codigo padronizado.

### Instalar o Black

Se ainda nao estiver instalado no ambiente virtual, execute:

```bash
pip install black
```

### Configurar o VS Code para usar o Black

Este projeto ja possui a configuracao no arquivo `.vscode/settings.json` com as opcoes abaixo:

```json
{
	"editor.formatOnSave": true,
	"python.formatting.provider": "black",
	"python.analysis.typeCheckingMode": "off"
}
```

Para abrir o arquivo de settings do do VS Code, digite 'CTRL' + 'SHIFT' + p, digite settings e procure por Open Workspace Settings (JSON), e informe as configurações acima.

Com isso, ao salvar um arquivo Python no VS Code, o editor aplica a formatacao automaticamente usando o Black.

### Formatar manualmente pelo terminal

Se quiser formatar um arquivo ou o projeto inteiro manualmente, use:

```bash
black .
```

Ou, para um unico arquivo:

```bash
black nome_do_arquivo.py
```

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
