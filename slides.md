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

<br>
<img src="/src/utfpr.png" class="m-0 h-20" />

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>

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

<footer class="absolute bottom--8 right--14">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
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

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
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

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

# Revisão da Literatura

<br>

Para atingir os objetivos da pesquisa:
- Foi realizada uma revisão bibliográfica de artigos que abordaram Descoberta de Conhecimento e Mineração de Dados a partir dos dados de acidentes da PRF
- As strings de busca utilizadas foram Policia Rodoviária Federal OR PRF AND análise OR correlação OR classificação
- Os resultados foram filtrados por meio da leitura dos resumos e leitura completa dos artigos
- Resultando em um total de 10 artigos que atenderam os critérios definidos

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

## Trabalhos que buscam correlações

<br>

<img src="/src/works_correlation.png" />

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

## Trabalhos que buscam classificações

<br>

<img src="/src/works_classification.png" />

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

# Desenvolvimento

<br>

O desenvolvimento deste trabalho consiste em alguns passos, separados em fases que
seguem o processo de Descoberta de Conhecimento em Bases de Dados ou KDD


<img src="/src/kdd.png" class="h-80" />

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

## Dados utilizados

<br>

<img src="/src/used_data.png" />
<small>Fonte: Dados abertos da Polícia Rodoviária Federal</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---
layout: two-cols
---

::default::

## Dados não utilizados

<br>

<img src="/src/non_used_data.png" />
<small>Fonte: Dados abertos da Polícia Rodoviária Federal</small>

::right::

## Razão para não utilização

<br>

* Inclusos em outros campos
* Obtidos após a ocorrência do acidente
* Necessitam de agentes externos para serem obtidos

<footer class="absolute bottom--10 right--14">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
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

<footer class="absolute bottom--10 right--14">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

### Feriados

<br>

<SlidevVideo autoPlay="resume" muted controls>
  <source src="/src/code_holidays.webm" type="video/webm">
</SlidevVideo>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

### Pedágios

<br>

<SlidevVideo autoPlay="resume" muted controls>
  <source src="/src/code_tolls.webm" type="video/webm">
</SlidevVideo>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

### Radares

<br>

<SlidevVideo autoPlay="resume" muted controls>
  <source src="/src/code_radars.webm" type="video/webm">
</SlidevVideo>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

### Resultado

<br>

<SlidevVideo autoPlay="resume" muted controls>
  <source src="/src/code_join.webm" type="video/webm">
</SlidevVideo>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

## Pré-Processamento

<br>

* Remoção de linhas que não possuíam a informação br e km (659 registros)
* Preenchimento de linhas sem valor (radares)
* Transformar dados categóricos em numéricos, pois os algoritmos trabalham melhor com dados numéricos
* Padronizar escala dos dados, para algoritmos que utilizam o plano cartesiano para cálculos de distância

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

### Remoção linhas sem br e km

<br>

<img src="/src/delete_cols_without_km_br.png" class="h-110" />

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

### Preencher linhas vazias

<br>

<img src="/src/fill_na_radars.png" class="h-100" />

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

### Transformar dados categóricos em numéricos

<br>

```python
from sklearn.preprocessing import LabelEncoder
labelencoder = LabelEncoder()
X_labeled_encoded = labelencoder.fit_transform(X_df)
```

<br>

### Padronizar escala dos dados

<br>

```python
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
scaler.fit(X_labeled_encoded)
df_scaled = scaler.transform(X_labeled_encoded)
```

<!--img src="/src/std_df.png" /-->

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

# Resultados e Discussão

## Cenários e experimentos

* 16 com separação entre dados de treino e teste
* 16 com validação cruzada
* Utilizando apenas as categorias com mais de 10 mil registros
* Com ou sem as colunas adicionadas
* Com ou sem balanceamento nos dados
  * RandomUnderSampler
  * NearMiss
  * OneSidedSelection
* Algoritmos
  * DecisionTree
  * RandomForest
  * K Nearest Neighbor

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

### Exemplo de caso de teste
> Separando os dados em treino e teste, com todas as colunas, todos os tipos de acidentes e sem realizar balanceamento

<br>

<SlidevVideo autoPlay="resume" muted controls class="h-100">
  <source src="/src/code_first_case.webm" type="video/webm">
</SlidevVideo>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

### Exemplo de caso de teste
> Validação cruzada, sem as colunas adicionadas, apenas com os acidentes com mais de 10 mil registros e com OneSidedSelection

<br>

<SlidevVideo autoPlay="resume" muted controls class="h-100">
  <source src="/src/code_last_case.webm" type="video/webm">
</SlidevVideo>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

## Resultados com separação de dados entre treino e teste

<br>

<img src="/src/train_test_result.png" class="h-110" />

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

## Resultados com validação cruzada

<br>

<img src="/src/cross_validation_result.png" class="h-110" />

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

# Considerações Finais

* A taxa geral de acurácia foi baixa
  * Possível falta de dados
  * Complexidade dos acidentes
  * Baixa representatividade das colunas adicionadas
    * feriados ~ 10%
    * radares < 3%
    * pedágio ~ 46%
* Sistematização da classificação de acidentes
* Aparenta ser um estudo inédito, como sugere a análise bibliográfica

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

# Trabalhos futuros

* Conjunto de dados maior e mais diversificado
* Inclusão de mais informações sobre as rodovias
* Explorar outras técnicas de aprendizado de máquinas

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

# Referências

<br>

IPEA, P. (2015). Acidentes de trânsito nas rodovias federais brasileiras caracterização, tendências e custos para a sociedade. Technical report, Instituto de PesquisaEconômica Aplicada (IPEA).

da Saúde OPS, O. P.-A. (2018). Salvar vidas – pacote de medidas técnicas para a segurança no trânsito. Technical report, Organização Mundial da Saúde (OMS).

Fernandes, F. T. and Chiavegatto, A. D. P. (2019). Perspectivas do uso de mineração de dados e aprendizado de máquina em saúde e segurança no trabalho. Revista Brasileira de Saúde Ocupacional [online], 44.

Moosavi, S., Samavatian, M. H., Parthasarathy, S., Teodorescu, R., and Ramnath, R. (2019). Accident risk prediction based on heterogeneous sparse data: New dataset and insights. In Proceedings of the 27th ACM SIGSPATIAL International Conference on Advances in Geographic Information Systems, SIGSPATIAL ’19, page 33–42, New York, NY, USA. Association for Computing Machinery.

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---