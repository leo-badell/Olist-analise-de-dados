# Análise de Dados — Olist

## Descrição do Projeto

Este projeto faz parte do curso de Machine Learning da SCTEC e tem como objetivo realizar o **pré-processamento e análise exploratória** do dataset público da [Olist], maior plataforma de e-commerce do Brasil.

O problema central abordado é a **qualidade dos dados brutos**: presença de valores nulos, inconsistências de formatação, strings mal padronizadas e campos de dimensão ausentes nos produtos — situações comuns em dados de produção que precisam ser tratadas antes de qualquer modelagem.

O objetivo dos scripts é entregar um conjunto de dados limpo, padronizado e confiável, que sirva de base sólida para futuros modelos de Machine Learning.

---

## Estrutura do Projeto

```text
 analise_olist/
 ├── 01_validacao_e_tratamento_de_dados_ausentes.ipynb
 ├── 02_padronizacao_de_strings_e_regex.ipynb
 ├── 03_logica_de_regra_de_negocio.ipynb
 ├── 04_formatacao_temporal_datetime.ipynb
 ├── 05_relatorio_de_status_manual.ipynb
 ├── orders.csv
 └── produtos_processados.csv
```

---

## Guia de Execução

### Pré-requisitos

- Python **3.12+** instalado
- [VS Code](https://code.visualstudio.com/) com a extensão **Jupyter** instalada

### Passo a passo

#### 1. Clone ou baixe o repositório

```bash
git clone <url-do-repositorio>
cd "Olist analise de dados"
```

#### 2. Crie e ative o ambiente virtual

```bash
# Criar
python -m venv .venv

# Ativar (Windows)
.venv\Scripts\activate
```

#### 3. Instale as dependências

```bash
pip install ipykernel pandas
```

> O `ipykernel` é obrigatório para que o VS Code consiga conectar os notebooks ao Python do ambiente virtual.

#### 4. Selecione o kernel correto no VS Code

- Abra qualquer notebook `.ipynb`
- Clique no seletor de kernel (canto superior direito)
- Escolha o interpretador dentro de `.venv` (Python 3.12.x)

#### 5. Execute os notebooks em ordem

Abra e execute cada notebook na sequência numérica:

| Ordem | Notebook | O que faz |
| ----- | -------- | --------- |
| 1 | `01_validacao_e_tratamento_de_dados_ausentes.ipynb` | Detecta e trata valores nulos |
| 2 | `02_padronizacao_de_strings_e_regex.ipynb` | Padroniza strings e aplica regex |
| 3 | `03_logica_de_regra_de_negocio.ipynb` | Aplica regras de negócio |
| 4 | `04_formatacao_temporal_datetime.ipynb` | Formata campos de data/hora |
| 5 | `05_relatorio_de_status_manual.ipynb` | Gera relatório de status do processamento |

#### 6. Verifique a saída

O notebook `05` imprime um relatório resumindo o total de linhas processadas, categorias corrigidas e campos nulos tratados — confirmando que o pipeline foi executado com sucesso.
