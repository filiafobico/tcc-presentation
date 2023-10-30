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

<br>
Orientando: Luis Eduardo Oliveira

Orientador: Prof. Dr. André Pinz Borges

---
layout: two-cols
---

::default::

# Agenda

* Introdução
* Objetivo Geral e Objetivos Específicos
* Revisão da Literatura
  * Trabalhos que buscam correlações
  * Trabalhos que buscam classificações
* Desenvolvimento
  * Dados utilizados
  * Dados não utilizados
  * Razão para não utilização
  * Dados adicionados
  * Fonte da informação
  * Fonte da informação
  * Pré-Processamento

::right::

<br>
<br>

* Resultados e Discussão
  * Cenários e experimentos
  * Testes com separação de dados entre treino e teste
  * Testes com validação cruzada
* Considerações Finais
* Trabalhos futuros

---

# Introdução

<br>

- Acidentes custam (2015), ao Brasil, R$ 40 bilhões por ano [IPEA 2015]
  - R$ 12 bilhões só em rodovias federais
- A princial causa de morte, entre pessoas de 15 a 29 anos, são acidentes [OPS 2018]

<br>

- Graças ao aumento da produção e categorização de dados, tornou-se possivel a utilização de técnicas de Mineração de Dados para tratar problemas complexos [Fernandes e Chiavegatto 2019]
- Existem exemplos, em outros países, de sistemas que tentam fazer a predição da ocorrência de um acidente em determinada via
  - Como o trabalho de [Moosavi et al. 2019] em que se tem um sistema alimetado em tempo real com dados de 2 fontes públicas. É utilizado aprendizagem de reforço e feita a comparação entre 3 modelos de Apredizagem de Máquina

---


# Objetivo Geral

<br>

Utilizando os informações disponibilizadas pela Polícia Rodoviária Federal, sem a utilização de dados que existem apenas após a ocorrência do acidente, classificar o tipo de acidente ocorrido


## Objetivos Específicos

<br>

- Compreender o conjunto de dados
- Aplicar as etapas da Descoberta de Conhecimento em Bases de Dados no conjunto de dados de acidentes da PRF
- Fazer uso de difentes modelos de classificação para obtenção de informações sobre acidentes
- Comparar os modelos obtidos

---

# Revisão da Literatura

<br>

Para atingir os objetivos da pesquisa:
- Foi realizada uma revisão bibliográfica de artigos que abordaram Descoberta de Conhecimento e Mineração de Dados a partir dos dados de acidentes da PRF
- As strings de busca utilizadas foram Policia Rodoviária Federal OR PRF AND análise OR correlação OR classificação
- Os resultados foram filtrados por meio da leitura dos resumos e leitura completa dos artigos
- Resultando em um total de 10 artigos que atenderam os critérios definidos

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

## Pré-Processamento

<br>

* Remoção de linhas que não possuíam a informação br e km (659 registros)
* Preenchimento de linhas sem valor (radares e pedágios)
* Transformar dados categóricos em numéricos, pois os algoritmos trabalham melhor com dados numéricos
* Padronizar escala dos dados, para algoritmos que utilizam o plano cartesiano para cálculos de distância

---

# Resultados e Discussão

## Cenários e experimentos

* 16 com separação entre dados de treino e teste
* 16 com validação cruzada
* Utilizando apenas as categorias com mais de 10 mil registros
* Com ou sem as clunas adicionadas
* Com ou sem balanceamento nos dados
  * RandomUnderSampler
  * NearMiss
  * OneSidedSelection
* Algoritmos
  * DecisionTree
  * RandomForest
  * K Nearest Neighbor

---

## Testes com separação de dados entre treino e teste

<br>

<img src="/src/train_test_result.png" class="h-110" />

---

## Testes com validação cruzada

<br>

<img src="/src/cross_validation_result.png" class="h-110" />

---

# Considerações Finais

* A taxa geral de acurácia foi baixa
  * Possível falta de dados
  * Complexidade dos acidentes
  * Baixa representatividade das colunas adicionadas
    * feriados ~ 10%
    * pedágio ~ 1,4%
    * radares < 3%
* Sistematização da classificação de acidentes
* Aparenta ser um estudo inédito, como sugere a análise bibliográfica

---

# Trabalhos futuros

* Conjunto de dados maior e mais diversificado
* Inclusão de mais informações sobre as rodovias
* Explorar outras técnicas de aprendizado de máquinas

---

# Referências

<br>

IPEA, P. (2015). Acidentes de trânsito nas rodovias federais brasileiras caracterização, tendências e custos para a sociedade. Technical report, Instituto de PesquisaEconômica Aplicada (IPEA).

da Saúde OPS, O. P.-A. (2018). Salvar vidas – pacote de medidas técnicas para a segurança no trânsito. Technical report, Organização Mundial da Saúde (OMS).

Fernandes, F. T. and Chiavegatto, A. D. P. (2019). Perspectivas do uso de mineração de dados e aprendizado de máquina em saúde e segurança no trabalho. Revista Brasileira de Saúde Ocupacional [online], 44.

Moosavi, S., Samavatian, M. H., Parthasarathy, S., Teodorescu, R., and Ramnath, R. (2019). Accident risk prediction based on heterogeneous sparse data: New dataset and insights. In Proceedings of the 27th ACM SIGSPATIAL International Conference on Advances in Geographic Information Systems, SIGSPATIAL ’19, page 33–42, New York, NY, USA. Association for Computing Machinery.

---