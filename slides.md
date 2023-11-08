---
theme: default
class: text-center
highlighter: shiki
lineNumbers: false
drawings:
  persist: false
transition: fade-out
title: TCC
record: true
---

# Comparação de modelos de predição de categorias de acidentes nas rodovias federais

<br>
Orientando: Luis Eduardo Oliveira

Orientador: Prof. Dr. André Pinz Borges

<br>
<img src="/src/utfpr.png" class="m-0 h-20" />

<small class="absolute bottom-15 right-5">Sumetido ao evento <a href="http://erigo.sbc.org.br/">XI ERI-GO</a></small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>

---

# Agenda

* Introdução
* Objetivo Geral e Objetivos Específicos
* Revisão da Literatura
* Desenvolvimento
* Resultados e Discussão
* Considerações Finais
* Trabalhos futuros

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>

---

# Introdução

<br>

- Acidentes custam R$ 40 bilhões por ano (IPEA, 2015)
  - R$ 12 bilhões só em rodovias federais
  - A principal causa de morte entre pessoas de 15 a 29 anos (OPS, 2018)

<br>

- Utilização de técnicas de Mineração de Dados para tratar problemas complexos (FERNANDES; CHIAVEGATTO, 2019)
  - Trabalho de (MOOSAVI et al., 2019) utiliza aprendizagem por reforço e faz a comparação entre 3 modelos de Apredizagem de Máquina

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>

<!--
De acordo com FERNANDES: com o aumento da produção e categorização de dados, torna-se possivel a utilização de técnicas de Mineração de Dados para tratar problemas complexos

Existem exemplos, em outros países, de sistemas que tentam fazer a predição da ocorrência de um acidente em determinada via
(MOOSAVI et al., 2019) em que foi criado um sistema alimetado em tempo real com dados de 2 fontes públicas. O trabalho utiliza aprendizagem por reforço e faz a comparação entre 3 modelos de Apredizagem de Máquina
-->

---

# Objetivo Geral

<br>

Classificar o tipo de acidente, utilizando informações disponibilizadas pela Polícia Rodoviária Federal, sem a utilização de dados que existem apenas após a ocorrência do acidente

## Objetivos Específicos

<br>

- Compreender o conjunto de dados
- Aplicar as etapas da Descoberta de Conhecimento em Bases de Dados no conjunto de dados de acidentes da PRF
- Fazer uso de difentes modelos de classificação
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
- A string de busca utilizada foi "Policia Rodoviária Federal OR PRF AND análise OR correlação OR classificação"
- Os resultados foram filtrados por meio da leitura dos resumos e leitura completa dos artigos
- Resultando em um total de 10 artigos que atenderam os critérios definidos

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>

---

## Trabalhos que buscam correlações

<br>
<small class="flex justify-center">Quadro 1. Dados dos trabalhos que buscam correlações</small>
<div class="flex justify-center items-center">
  <img src="/src/works_correlation.png" class="h-90" />
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>


---

## Trabalhos que buscam classificações

<br>
<small class="flex justify-center">Quadro 2. Dados de trabalhos que buscam classificações</small>
<div class="flex justify-center items-center">
  <img src="/src/works_classification.png" class="h-90" />
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>


---

# Desenvolvimento

<br>

<p></p>
<small class="flex justify-center">Figura 1. Passos do KDD</small>
<div class="flex justify-center items-center">
  <img src="/src/kdd.png" class="h-80" />
</div>
<small class="flex justify-center">Fonte: Adaptado de Fayyad et al. 1996</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>

<!--
O desenvolvimento deste trabalho consiste em alguns passos, separados em fases que
seguem o processo de Descoberta de Conhecimento em Bases de Dados ou KDD
-->

---

## Ferramentas utilizadas

<br>

* MongoDBAtlas
* MongoDBCompass
* Google Colab
* Python
  * pandas
  * numpy
  * imblearn
  * sklearn

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>

---

## Dados utilizados

<br>
<small class="flex justify-center">Quadro 3. Dados da PRF</small>
<div class="flex justify-center items-center">
  <img src="/src/used_data.png" class="h-90" />
</div>
<small class="flex justify-center">Fonte: Dados abertos da Polícia Rodoviária Federal</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>

---

## Tipo dos dados

<br>

* data_inversa - *ex: 2021-01-01*
* dia_semana - *ex: sexta-feira*
* br - *ex: 101*
* km - *ex: 314.9*
* uf - *ex: PR*
* fase_dia - *Plena Noite, Anoitecer, Pleno dia, Amanhecer*
* condicao_metereologica - *Chuva, Nublado, Céu Claro, Vento, Neve, Granizo, Nevoeiro/Neblina, Sol, Ignorado, Garoa/Chuvisco*
* tipo_acidente - *Colisão traseira, Colisão com objeto, Incêndio, Colisão lateral, Saída de leito carroçável, Atropelamento de Pedestre, Colisão frontal, Capotamento, Atropelamento de Animal, Tombamento, Colisão transversal, Queda de ocupante de veículo, Colisão lateral mesmo sentido, Colisão lateral sentido oposto, Engavetamento, Derramamento de carga, Eventos atípicos, Colisão com objeto estático, Colisão com objeto em movimento, Danos eventuais*

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
<small class="flex justify-center">Quadro 4. Dados da PRF não utilizadas</small>
<div class="flex justify-center items-center">
  <img src="/src/non_used_data.png" />
</div>
<small class="flex justify-center">Fonte: Dados abertos da Polícia Rodoviária Federal</small>

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

<!--
1. São campos que a informação já existe em uma das colunas que serão utilizadas. Como horário que está incluso no campos de fase_dia.

2. São campos que a informação só existe após a ocorrência do acidente, como a causa do acidente.

A proposta do trabalho é justamente tentar generalizar um modelo para prever um acidente, então não teria como utilizar os dados que existem apenas após a ocorrencia do acidente.

3. São informações que precisariam de algum tipo de sensor para captar em tempo real, como quantidade de carros no trecho ou quantidade de pessoas envolvidas.
-->

---
layout: two-cols
---

::default::

## Dados adicionados

<br>
<small class="flex justify-center">Quadro 5. Colunas adicionadas</small>
<div class="flex justify-center items-center">
  <img src="/src/added_data.png" />
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>

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
<small class="flex justify-center">Codigo 1. Algoritmo de enriquecimento de dados com a informação de feriados</small>
<div class="flex justify-center items-center">
  <SlidevVideo autoPlay="resume" muted controls>
    <source src="/src/code_holidays.webm" type="video/webm">
  </SlidevVideo>
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>


---

### Pedágios

<br>
<small class="flex justify-center">Codigo 2. Algoritmo de enriquecimento de dados com a informação de feriados</small>
<div class="flex justify-center items-center">
  <SlidevVideo autoPlay="resume" muted controls>
    <source src="/src/code_tolls.webm" type="video/webm">
  </SlidevVideo>
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>


---

### Radares

<br>
<small class="flex justify-center">Codigo 3. Algoritmo de enriquecimento de dados com a informação de radares</small>
<div class="flex justify-center items-center">
  <SlidevVideo autoPlay="resume" muted controls>
    <source src="/src/code_radars.webm" type="video/webm">
  </SlidevVideo>
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>


---

### Resultado

<br>
<small class="flex justify-center">Codigo 4. Algoritmo para enriquecimento da base original</small>
<div class="flex justify-center items-center">
  <SlidevVideo autoPlay="resume" muted controls class="h-95">
    <source src="/src/code_join.webm" type="video/webm">
  </SlidevVideo>
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>


---

## Demais etapas do pré-processamento

<br>

* Remover linhas que não possuíam a informação br e km (659 instâncias)
  * Correspondente a < 0,2% da base original (343.327 mil instâncias)
* Preencher linhas sem valor (radares)
* Transformar dados categóricos em numéricos, pois os algoritmos trabalham melhor com dados numéricos
  * LabelEncoder
* Normalizar os dados para algoritmos que utilizam o plano cartesiano para cálculos de distância
  * StandardScaler

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>

---

### Remoção linhas sem br e km

<br>
<small class="flex justify-center">Remoção de linhas sem valores</small>
<div class="flex justify-center items-center">
  <img src="/src/delete_cols_without_km_br.png" class="h-95" />
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>


<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>


---

### Preencher linhas sem valor

<br>
<small class="flex justify-center">Codigo 5. Algoritmo para preenchimento de linhas sem valor</small>
<div class="flex justify-center items-center">
  <img src="/src/fill_na_radars.png" class="h-100" />
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>


---

# Resultados e Discussão

## Cenários
<br>

* Base enriquecida possui 342.668 mil instâncias e 10 atributos
* 16 com separação entre dados de treinamento e teste (70% x 30%)
* 16 com validação cruzada
* Utilizando apenas as categorias com mais de 10 mil registros
> Atropelamento de Animal, Incêndio, Engavetamento, Colisão lateral mesmo sentido, Colisão com objeto, Colisão com objeto em movimento, Colisão lateral sentido oposto, Derramamento de carga, Danos eventuais, Eventos atípicos
* Com ou sem as colunas adicionadas
* Com ou sem balanceamento nos dados
  * RandomUnderSampler, NearMiss, OneSidedSelection
* Algoritmos
  * DecisionTree, RandomForest, K-Nearest Neighbor

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>

<!--
o balanceamento utilizado fora o undersampling, que tem o objetivo de reduzir as colunas com mais dados para que o dataset não fique muito desigual.

- Random
Deixa todas as categorias com o tamanho da menor categoria, escolhendo os dados ficam de forma aleatória.

- NearMiss
Funciona similar ao Random, mas utiliza euristicas, como KDD, para decidir quais dados fiocam na no conjunto resultante.

- OneSidedSelection
Também diminui o tamanho das classes, mas não deixa todas do mesmo tamanho.
Utiliza euristicas mais finas para tratar os dados como casos que redundantes, ou outliers.

https://www.researchgate.net/publication/226859454_Applying_One-Sided_Selection_to_Unbalanced_Datasets
-->

---

### Exemplo de caso de teste
> Separando os dados em treino e teste, com todas as colunas, todos os tipos de acidentes e sem realizar balanceamento

<br>
<small class="flex justify-center">Código 6. Caso de teste sem tratativa nos dados</small>
<div class="flex justify-center items-center">
  <SlidevVideo autoPlay="resume" muted controls class="h-90">
    <source src="/src/code_first_case.webm" type="video/webm">
  </SlidevVideo>
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>


---

### Exemplo de caso de teste
> Validação cruzada, sem as colunas adicionadas, apenas com os acidentes com mais de 10 mil registros e com OneSidedSelection

<br>
<small class="flex justify-center">Código 7. Caso de teste com tratativas nos dados</small>
<div class="flex justify-center items-center">
  <SlidevVideo autoPlay="resume" muted controls class="h-90">
    <source src="/src/code_last_case.webm" type="video/webm">
  </SlidevVideo>
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>


---

## Resultados com separação de dados entre treino e teste

<br>
<small class="flex justify-center">Tabela 1. Resultados com separação de dados entre treino e teste</small>
<div class="flex justify-center items-center">
  <img src="/src/train_test_result.png" class="h-100" />
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>


---

## Resultados com validação cruzada

<br>
<small class="flex justify-center">Tabela 2. Resultados com validação cruzada</small>
<div class="flex justify-center items-center">
  <img src="/src/cross_validation_result.png" class="h-100" />
</div>
<small class="flex justify-center">Fonte: Autoria própria</small>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>


---

# Discussão

<br>

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

# Considerações Finais

<br>

* Compreender o conjunto de dados
* Aplicar as etapas da Descoberta de Conhecimento em Bases de Dados no conjunto de dados de acidentes da PRF
* Fazer uso de difentes modelos de classificação
* Comparar os modelos obtidos

Classificar o tipo de acidente, utilizando informações disponibilizadas pela Polícia Rodoviária Federal, sem a utilização de dados que existem apenas após a ocorrência do acidente

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>

<!--
> Objetivo atingido com a realização do trabalho
> Fora aplicado os passos do KDD que contribuiu para o desenvolvimento da pesquisa
> Foram utilizados 3 modelos diferentes
> Fora comparado os 32 casos de testes e apontado os melhores resultados

Apesar da taxa de acerto ser baixa, o que se propôs foi realizado
-->

---

# Trabalhos futuros

* Conjunto de dados maior e mais diversificado
* Inclusão de mais informações sobre as rodovias, como dados de radares móveis
* Explorar outras técnicas de Aprendizagem de Máquina
* Agrupar os tipos de acidentes para reduzir a quantidade de categorias

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
---

# Referências

<br>

IPEA, P. (2015). Acidentes de trânsito nas rodovias federais brasileiras caracterização, tendências e custos para a sociedade. Technical report, Instituto de Pesquisa Econômica Aplicada (IPEA).

da Saúde OPS, O. P.-A. (2018). Salvar vidas – pacote de medidas técnicas para a segurança no trânsito. Technical report, Organização Mundial da Saúde (OMS).

Fernandes, F. T. and Chiavegatto, A. D. P. (2019). Perspectivas do uso de mineração de dados e aprendizado de máquina em saúde e segurança no trabalho. Revista Brasileira de Saúde Ocupacional [online], 44.

Moosavi, S., Samavatian, M. H., Parthasarathy, S., Teodorescu, R., and Ramnath, R. (2019). Accident risk prediction based on heterogeneous sparse data: New dataset and insights. In Proceedings of the 27th ACM SIGSPATIAL International Conference on Advances in Geographic Information Systems, SIGSPATIAL ’19, page 33–42, New York, NY, USA. Association for Computing Machinery.

Fayyad, U., Piatetsky-Shapiro, G., and Smyth, P. (1996). From data mining to knowledge
discovery in databases. AI Magazine, 17(3):37

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>

---

<div class="h-full flex justify-center items-center gap-2">
  <h1> Obrigado </h1>
</div>

<footer class="absolute bottom-0 right-0">
  <br/>
  <small><SlideCurrentNo/>/<SlidesTotal/></small>
</footer>
