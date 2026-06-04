# PIJunior Trainee

Projeto desenvolvido utilizando Python, SeleniumBase e gerenciamento de dependências com UV.

## Pré-requisitos

Antes de executar o projeto, instale:

* Python 3.12 ou superior
* UV
* Google Chrome ou Mozilla Firefox

---

## Clonando o projeto

```bash
git clone <URL_DO_REPOSITORIO>
cd pijunior-trainee
```

---

## Instalando as dependências

O projeto utiliza o arquivo `uv.lock` para garantir versões consistentes das dependências.

Execute:

```bash
uv sync
```

Esse comando criará o ambiente virtual e instalará todas as dependências necessárias.

---

## Ativando o ambiente virtual

Linux/macOS:

```bash
source .venv/bin/activate
```

Windows:

```powershell
.venv\Scripts\activate
```

---

## Executando a aplicação

Opção 1: VS Code + Extensão Jupyter (Recomendado)

Este projeto pode ser executado diretamente pelo VS Code utilizando a extensão Jupyter.

1) Instale as extensões:
- Python (Microsoft)
- Jupyter (Microsoft)
2) Abra a pasta do projeto no VS Code.
3) Instale as dependências:
uv sync
4) Abra o arquivo login.ipynb.
5) Selecione o kernel Python do ambiente virtual criado pelo UV (.venv).
6) Execute as células normalmente utilizando os botões do Jupyter ou Shift + Enter.

Caso o ambiente virtual não apareça automaticamente, selecione:

Python Environment -> .venv

ou informe manualmente o interpretador:

.venv/bin/python        (Linux/macOS)
.venv\Scripts\python.exe (Windows)

---

# Fluxo de Trabalho com Git

Este projeto segue um fluxo simples baseado em GitFlow.

## Branch principal

A branch `main` contém apenas código estável.

Nenhuma alteração deve ser feita diretamente nela.

---

## Criando uma branch de funcionalidade

Antes de iniciar uma tarefa:

```bash
git switch main
git pull origin main
git switch -c feature/nome-da-feature
```

Exemplo:

```bash
git switch -c feature/login
```

---

## Realizando alterações

Após implementar a funcionalidade:

```bash
git add .
git commit -m "Implementa automação de login"
```

---

## Enviando para o GitHub

Na primeira vez:

```bash
git push -u origin feature/login
```

Nos próximos envios:

```bash
git push
```

---

## Abrindo um Pull Request

Após enviar a branch:

1. Acesse o repositório no GitHub.
2. Clique em **Compare & Pull Request**.
3. Descreva as alterações realizadas.
4. Solicite revisão, se necessário.
5. Aguarde aprovação e merge.

---

## Atualizando sua branch com a main

Caso a branch principal tenha recebido novas alterações:

```bash
git switch main
git pull origin main

git switch feature/login
git merge main
```

---

## Comandos úteis

Verificar status:

```bash
git status
```

Listar branches:

```bash
git branch
```

Ver histórico:

```bash
git log --oneline --graph --all
```

Enviar alterações:

```bash
git push
```

Baixar alterações:

```bash
git pull
```
