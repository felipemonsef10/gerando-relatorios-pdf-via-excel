# Gerando Relatórios PDF via Excel

**Autor:** felipemonsef10
**Linguagem:** Python

## Resumo

Este projeto implementa um pipeline automatizado para a transformação de dados tabulares, armazenados em planilhas Excel, em documentos PDF formatados e prontos para distribuição. A proposta central é eliminar a intervenção manual na etapa de composição de relatórios periódicos, substituindo-a por um processo determinístico de extração, transformação e renderização de dados (ETL aplicado à geração documental).

## Sumário

1. [Introdução](#introdução)
2. [Arquitetura do Sistema](#arquitetura-do-sistema)
3. [Tecnologias e Dependências](#tecnologias-e-dependências)
4. [Instalação](#instalação)
5. [Modo de Uso](#modo-de-uso)
6. [Estrutura do Repositório](#estrutura-do-repositório)
7. [Limitações e Trabalhos Futuros](#limitações-e-trabalhos-futuros)

## Introdução

A geração manual de relatórios a partir de planilhas eletrônicas é uma tarefa recorrente em contextos administrativos e financeiros, mas sujeita a erros humanos e a baixa reprodutibilidade. Este projeto propõe uma solução programática que lê os dados de origem, aplica regras de formatação e produz um documento PDF com layout consistente, reduzindo o tempo de execução da tarefa e garantindo padronização entre diferentes execuções.


## Arquitetura do Sistema

O repositório segue uma organização funcional simples, na qual cada módulo é responsável por uma etapa isolada do pipeline (leitura, processamento, formatação e geração do documento), favorecendo a separação de responsabilidades e a manutenibilidade do código.

## Tecnologias e Dependências

| Categoria | Ferramenta |
| :--- | :--- |
| Linguagem | Python 3 |
| Manipulação de dados | pandas / openpyxl |
| Geração de PDF | pdfkit / wkhtmltopdf |
| Gerenciamento de dependências | requirements.txt |

> ⚠️ Recomenda-se consultar o arquivo `requirements.txt` do repositório para a lista definitiva e versionada das dependências, dado que este README foi elaborado a partir de uma inspeção geral da estrutura do projeto.

## Instalação

```bash
# Clonar o repositório
git clone https://github.com/felipemonsef10/gerando-relatorios-pdf-via-excel.git
cd gerando-relatorios-pdf-via-excel

# Criar e ativar um ambiente virtual (recomendado)
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

# Instalar as dependências
pip install -r requirements.txt
```

## Modo de Uso

```bash
python gerar_relatorio.py
```

Certifique-se de que o arquivo de entrada (planilha `.xlsx`) esteja no diretório esperado pelo script antes da execução. O relatório em PDF será gerado como saída do processo.

## Estrutura do Repositório

```
gerando-relatorios-pdf-via-excel/
├── gerar_relatorio.py         # Ponto de entrada do pipeline
├── requirements.txt           # Dependências do projeto
└── ...                        # Módulos auxiliares de processamento e formatação
```

## Limitações e Trabalhos Futuros

* Ausência de testes automatizados documentados para validação do pipeline.
* Ausência de um arquivo de licença formal (ver observação abaixo).
* Possibilidade de extensão para múltiplos formatos de saída (ex.: `.docx`, `.html`).