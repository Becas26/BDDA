# **BDDA - Bases de Dados Distribuídas Avançadas**  
_Relatório: Componente Técnica_

### Tempo para entrega do projeto:

![Countdown Timer](https://i.countdownmail.com/3w7q9r.gif)

---

## **Trabalho realizado por:**
- **Diogo Freitas** (104841)  
- **João Francisco Botas** (104782)  
- **Rebeca Sampaio** (126628)

---

## **Índice**
1. [Introdução](#introdução)
2. [Descrição dos conjuntos de dados a utilizar](#descrição-dos-conjuntos-de-dados-a-utilizar)
3. [Metodologia e stack Hadoop](#metodologia-e-stack-hadoop)
4. [Análise ao utilizar a imagem Hue](#análise-ao-utilizar-a-imagem-hue)
5. [Conclusão](#conclusão)

---

## **Introdução**
> **Objetivo**: Apresentar um relatório sobre o uso de bases de dados distribuídas avançadas no contexto do projeto desenvolvido.
Neste relatório, vamos contextualizar as seguintes etapas:
- A descrição dos 2 datasets utilizados;
- As técnicas empregadas pré-análise dados;
- As visualizações retiradas após visualizar os 2 datasets.

---

## **Descrição dos conjuntos de dados a utilizar**
### Dataset 1: _artist_details_
Como primeiro dataset decidimos, através da API do Spotify, extrair [informações dos artistas](https://developer.spotify.com/documentation/web-api/reference/get-an-artist). Para a seleção dos artistas que iríamos recolher, decidimos retirá-los segundo um link do Kaggle que já agrupava o nome dos artistas e o país dos mesmos. 
- **Fonte do Kaggle**: [Link para o Dataset](https://www.kaggle.com/datasets/hedizekri/top-charts-artists-country)

Após esta fase, o processo subjacente à recolha e preparação dos dados foi executado um pouco da mesma maneira que o _publisher_ deste dataset fez.
- Inspirar num dataset existente (do próprio _publisher_);
- Retirar os dados da API oficial do Spotify;
- Fazer um hand-scrapping a linhas incoerentes ou com dados omissos que a API não recolheu bem.

**Descrição**:
Embaixo podemos ver um exemplo do dataset final
  
| Id         | Type         | Description                           |
|----------------|--------------|-------------------------------------|
| `artist_id`      | string      | Id único para o artista (do próprio Spotify)          |
| `artist_name`      | string | Nome do artista (apenas artistas solo) |
| `gender`      | string | Género do Artista |
| `age`      | int | Idade do artista (pode ter algumas incoerências) |
| `country_born`      | string | País em que o artista nasceu          |
| `followers`      | int | Número de seguidores que o artista tem no Spotify          |
| `popularity`      | int | Nível de popularidade do artista medido de 0 a 100          |
| `genres`      | array | Lista de todos os géneros de música do artista          |
| `image_url`      | string | Imagem do artista no Spotify (apenas para confirmar a identidade no processo de limpeza)          |


**Exemplo de Dados** (com _header_):
```csv
artist_name,gender,age,country_born,artist_id,followers,popularity,genres,image_url
Drake,male,37.0,Canada,3TVXtAsR1Inumwj472S9r4,94924678.0,97.0,"canadian hip hop, canadian pop, hip hop, pop rap, rap",https://i.scdn.co/image/ab6761610000e5eb4293385d324db8558179afd9
Post Malone,male,29.0,United States,246dkjvS1zLTtiykXe5h60,46205845.0,91.0,"dfw rap, melodic rap, pop, rap",https://i.scdn.co/image/ab6761610000e5ebe17c0aa1714a03d62b5ce4e0
Ed Sheeran,male,33.0,United Kingdom,6eUKZXaKkcviH0Ku9w2n3V,118303036.0,90.0,"pop, singer-songwriter pop, uk pop",https://i.scdn.co/image/ab6761610000e5eb784daff754ecfe0464ddbeb9
```
### Dataset 2: _artist_tracks_


## **Metodologia e stack Hadoop**
Para a realização deste projeto foi utilizado um /[dockercompose.yml](https://github.com/Vullkano/BDDA/blob/main/docker-compose.yml) que utiliza imagens do DockerHub, ou seja, a estrutura já vem pré-montada.

- ...

## **Análise ao utilizar a imagem Hue**

O processo desenvolvido nesta fase pode ser encontrado na seguinte [pasta](https://github.com/Vullkano/BDDA/tree/main/docs/relatorios/relatorio%20pratico%20imgs).



