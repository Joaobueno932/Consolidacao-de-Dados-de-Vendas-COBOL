# Consolidação de Dados de Vendas – COBOL

## Visão Geral

Este projeto consolida dados de vendas de múltiplos arquivos em um único arquivo unificado e gera um relatório com totais por região e gerais.
Simula um cenário comum em empresas que precisam integrar dados vindos de diferentes regiões ou sistemas.

## Funcionalidades

* **Leitura de múltiplos arquivos** (`SALES_REGION1.DAT` e `SALES_REGION2.DAT`)
* **Consolidação de dados** em um único arquivo (`CONSOLIDATED_SALES.DAT`)
* **Cálculo de totais** gerais e por região (quantidade e valor)
* **Geração de relatório** (`SALES_SUMMARY.RPT`) com:

  * Detalhes de cada transação
  * Sumários por região
  * Totais gerais de vendas

## Estrutura de Arquivos

* `SALESCON.COB` – Código-fonte do programa
* `SALES_REGION1.DAT` – Vendas da Região 1
* `SALES_REGION2.DAT` – Vendas da Região 2
* `CONSOLIDATED_SALES.DAT` – Arquivo consolidado
* `SALES_SUMMARY.RPT` – Relatório final

## Formato dos arquivos de entrada

* Posições 1–10: Região
* Posições 11–20: ID do Produto
* Posições 21–25: Quantidade
* Posições 26–32: Valor (2 casas decimais implícitas, ex.: 50000 = 500,00)

## Como Executar

**Pré-requisito:** compilador COBOL (ex.: GnuCOBOL)

1. Acesse a pasta do projeto:

   ```bash
   cd cobol_projects/sales_data_consolidation
   ```
2. Crie os arquivos `SALES_REGION1.DAT` e `SALES_REGION2.DAT` no formato acima.
3. Compile:

   ```bash
   cobc -x SALESCON.COB
   ```
4. Execute:

   ```bash
   ./SALESCON
   ```
5. Confira:

   * `CONSOLIDATED_SALES.DAT`
   * `SALES_SUMMARY.RPT`

## Habilidades demonstradas

* Leitura e processamento de múltiplos arquivos
* Consolidação de dados de diferentes origens
* Cálculo de totais gerais e por grupo
* Geração de relatórios com detalhes e sumários
* Operações aritméticas com dados numéricos
* Controle de fluxo com `IF` e `PERFORM`