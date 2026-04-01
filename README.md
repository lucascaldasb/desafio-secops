# Desafio SecOps

Este projeto foi desenvolvido como parte de um desafio prático com foco em **boas práticas de segurança, qualidade de código e automação de CI/CD** em uma aplicação Django.

A proposta principal foi aplicar ferramentas de análise estática, correções de segurança e garantir que a aplicação pudesse ser validada automaticamente em pipeline.

---

# Objetivos do desafio

Durante a execução do desafio foram aplicados os seguintes pontos:

* Configuração do ambiente Python com Poetry
* Execução local da aplicação Django
* Correção de problemas apontados por linters
* Análise de segurança com Bandit
* Criação de pipeline CI com GitHub Actions
* Versionamento com Git/GitHub

---

# Tecnologias utilizadas

* Python
* Django
* Poetry
* Ruff
* Bandit
* GitHub Actions

---

# Como executar o projeto

## 1. Clonar o repositório

```bash
git clone https://github.com/lucascaldasb/desafio-secops.git
cd desafio-secops
```

## 2. Instalar dependências

```bash
poetry install
```

## 3. Ativar ambiente virtual

```bash
poetry shell
```

## 4. Rodar servidor local

```bash
poetry run python manage.py runserver
```

ou com Docker

```bash
docker-compose up --build
```

---

# Qualidade e segurança do código

## Ruff (lint)

```bash
poetry run ruff check .
```

## Bandit (análise de segurança)

```bash
poetry run bandit -r core manage.py
```

---

# Evidências da execução

## Aplicação rodando localmente com Docker

![Aplicação rodando](./images/print-local.png)


![Aplicação rodando 2](./images/print-local-terminal.png)

## Bandit executado com análise de segurança

![Bandit](./images/print-bandit.png)

## Pipeline CI executando no GitHub Actions

![CI](./images/print-ci.png)

---

# Melhorias aplicadas

Durante o desafio foram feitas correções como:

* Remoção de SECRET_KEY hardcoded
* Uso de variáveis de ambiente
* Ajuste de imports no settings.py
* Correção de lint apontado pelo Ruff

---

# Observações

O projeto foi executado em ambiente Linux utilizando máquina virtual Ubuntu via VirtualBox.

---

# Autor

Lucas Caldas
