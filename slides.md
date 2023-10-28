---
theme: default
class: text-center
highlighter: shiki
lineNumbers: false
drawings:
  persist: false
transition: fade-out
title: TCC
---

# Comparação de modelos de predição de categorias de acidentes nas rodovias federais

Luis Eduardo Oliveira

---

# Introdução

<br>

- Acidentes custam, ao Brasil, R$ 40 bilhões por ano
  - R$ 12 bilhões só em rodovias federais
- A princial causa de morte, entre pessoas de 15 a 29 anos, são acidentes

<br>

- Graças ao aumento da produção e categorização de dados, tornou-se possivel a utilização de técnicas de mineração de dados para tratar problemas complexos
- Existem exemplos, em outros países, de sistemas que tentam fazer a predição da ocorrência de um acidente em determinada via

---
layout: two-cols
---

::default::

# Objetivo Geral

<br>

Utilizando os informações disponibilizadas pela Polícia Rodoviária Federal, sem a utilização de dados que existem apenas após a ocorrência do acidente, classificar o tipo de acidente ocorrido

::right::

# Objetivos Específicos

<br>

- Enriquecer os dados
- Fazer uso de difentes modelos de classificação afim de encontrar o que melhor se encaixa nos dados
---

# Revisão da Literatura

<br>

Para atingir os objetivos da pesquisa, foi realizada uma revisão bibliográfica de artigos
que abordaram Descoberta de Conhecimento e Mineração de Dados a partir dos dados
de acidentes da PRF. As strings de busca utilizadas foram **Policia Rodoviária Federal**
OR **PRF** AND **análise** OR **correlação** OR **classificação**. Os resultados foram
filtrados por meio da leitura dos resumos e leitura completa dos artigos, resultando em
um total de 10 artigos que atenderam os critérios definidos

---

## Trabalhos que buscam correlações

<br>

<img src="/src/works_correlation.png" />

---

## Trabalhos que buscam classificações

<br>

<img src="/src/works_classification.png" />

---

# Desenvolvimento

<br>

O desenvolvimento deste trabalho consiste em alguns passos, separados em fases que
seguem o processo de Descoberta de Conhecimento em Bases de Dados ou KDD

---

## Dados utilizados

<br>

<img src="/src/used_data.png" />

---
layout: two-cols
---

::default::

## Dados não utilizados

<br>

<img src="/src/non_used_data.png" />

::right::

## Razão para não utilização

<br>

* Inclusos em outros campos
* Obtidos após a ocorrência do acidente
* Necessitam de agentes externos para serem obtidos

---
layout: two-cols
---

::default::

## Dados adicionados

<br>

<img src="/src/added_data.png" />

::right::

## Fonte da informação

<br>

* Diário Oficial do Distrito Federal (PDF)
* Associação Brasileira de Concessionárias de Rodovias (Planilha)
* Departamento Nacional de Infraestrutura de Transportes (API)

---

## Sanitização

<br>

* Remoção de linhas que não possuíam a informação br e km (659 registros)
---

# Resultados e Discussão

---

# Considerações Finais

---
