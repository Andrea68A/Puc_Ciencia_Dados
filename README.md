# Sobre o MVP de Engenharia de Dados - dataset Netflix de filmes e seriados

Este projeto visa analisar o catálogo global de filmes e séries da Netflix para identificar tendências temporais, distribuição por gênero/país e métricas de desempenho. O objetivo é criar um pipeline de dados que transforme dados brutos em consultas que forneçam subsídios às tomadas de decisão. Foi utilizada a tecnologia em nuvem Databricks Comunity Edition, que permite a criação de cluster para a construção de pipelines de dados. O projeto envolve a busca, coleta, modelagem, carga e análise de dados.

O dataset Netflix Movies and TV Shows contém as produções lançadas entre 1925 e 2021 e encontra-se em: https://www.kaggle.com/datasets/shivamb/netflix-shows?select=netflix_titles.csv.


# Relatório do MVP 

Este documento fornece um relatório contendo a visão geral do problema a ser resolvido, a descrição da estrutura do trabalho, as evidências, a autoavaliação e as conclusões.

https://github.com/Andrea68A/Puc_Ciencia_Dados/blob/MVP_Engenharia_Dados/Relatorio_MVP_Engenharia%20de%20Dados.pdf




# Link Público GitHub para o MVP de Engenharia de Dados

https://github.com/Andrea68A/Puc_Ciencia_Dados/tree/MVP_Engenharia_Dados - repositório para o MVP de Engenharia de Dados

# Arquivo raw armazenado no Github

Arquivo armazenado em formato csv: https://raw.githubusercontent.com/Andrea68A/Puc_Ciencia_Dados/refs/heads/MVP_Engenharia_Dados/netflix_titles.csv

Referência: https://www.kaggle.com/datasets/shivamb/netflix-shows?select=netflix_titles.csv


# Catálogo camada gold

https://github.com/Andrea68A/Puc_Ciencia_Dados/blob/MVP_Engenharia_Dados/Catalogo_camada_gold_versao2.pdf


# Diagrama Modelo Floco de Neve Netflix – Camada Gold – MVP

https://github.com/Andrea68A/Puc_Ciencia_Dados/blob/MVP_Engenharia_Dados/Modelo_Floco_Neve_Netflix_MVP.pdf


# Links para os notebooks ipynb no Github:

https://github.com/Andrea68A/Puc_Ciencia_Dados/blob/MVP_Engenharia_Dados/000_Configurar_DBFS_e_pastas.ipynb
https://github.com/Andrea68A/Puc_Ciencia_Dados/blob/MVP_Engenharia_Dados/001_Importar_arquivos_raw.ipynb
https://github.com/Andrea68A/Puc_Ciencia_Dados/blob/MVP_Engenharia_Dados/002_Carregar_Camada_Bronze.ipynb
https://github.com/Andrea68A/Puc_Ciencia_Dados/blob/MVP_Engenharia_Dados/003_Transformacoes_Camada_Silver_floco_neve.ipynb
https://github.com/Andrea68A/Puc_Ciencia_Dados/blob/MVP_Engenharia_Dados/004_Camada_Gold_Floco_Neve.ipynb


# Links públicos no Databricks Community Edition, onde se encontram os notebooks:

Obs: Todos estes notebooks se encontram em https://github.com/Andrea68A/Puc_Ciencia_Dados/tree/MVP_Engenharia_Dados. Os links abaixo são evidências da criação dos notebooks no ambiente Databricks.

## Notebook 000_Configurar_DBFS_e_pastas.ipynb

Este notebook é voltado para inicialização de valores e criação de pastas. Deve ser o primeiro a ser executado.

Link para o notebook: https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/3814572266302145/815525683663273/8959396615508843/latest.html

## Notebook 001_Importar_arquivos_raw.ipynb

Este notebook tem como objetivo importar o dataset Kaggle sobre os filmes e seriados da Netflix, para o ambiente do Databricks. É o segundo a ser executado.

Link para notebook: https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/3814572266302145/4470911049895348/8959396615508843/latest.html


## Notebook 002_Carregar_Camada_Bronze.ipynb

Este notebook consiste na ingestão do arquivo csv para uma tabela em formato delta. Não há qualquer modificação, apenas recepção dos dados brutos. É O terceiro a ser executado.

Link para notebook: https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/3814572266302145/910373024565501/8959396615508843/latest.html


## Notebook 003_Transformacoes_Camada_Silver_floco_neve.ipynb

Este notebook é voltado para a limpeza, transformação e padronização dos dados. Abrange também o tratatamento de nulos e normalização de tabelas. É o quarto a ser executado. 

Link para o notebook: https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/3814572266302145/4178132741742921/8959396615508843/latest.html


## Notebook 004_Camada_Gold_Floco_Neve.ipynb

Este notebook tem como objetivo realizar agregações analíticas, análise temporal e consultas de métricas de desempenho (ranqueamento). É o último a ser executo.

Link para o notebook: https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/3814572266302145/2676970212451849/8959396615508843/latest.html



# Visão geral

Este MVP possibilita a resposta às seguintes questões:

1) Domínio temporal – conteúdos lançados entre 1925 e 2021 - distribuição de Conteúdo por ano de lançamento e tipo (“Movie” / “TV Show”), incluindo a média de duração (minutos ou temporadas) - análise temporal pode fornecer subsídios para retenção de usuários e para a criação de conteúdos, se as produções têm duração adequada.

A consulta exibe a distribuição de conteúdo, agrupada por tipo de conteúdo ("Movie" ou "TV Show") e ano de lançamento.
São exibidos os valores totais de cada tipo de contéudo e duração média.
Se for filme ("Movie"), a duração é expressa em minutos. Se o tipo de conteúdo for "TV Show", a duração é expressa em número de temporadas

2)	Quantidade de lançamentos de produções (filmes e séries) agrupados por mês e ano – possibilita a análise de tendências históricas e verificar quais meses têm mais lançamentos. Esta análise é utilizada para a gestão planejar os lançamentos anuais, de acordo com os meses e tipos de conteúdo (filmes e séries).

3)	Quantidade de títulos por ano, agrupada por tipo de conteúdo em forma tabular e gráfica. Esta análise gráfica permite avaliar a tendência de crescimento nas quantidades de lançamentos, por exemplo, se há crescimento linear, aumento exponencial, decréscimo.

4)	Distribuição de classificações etárias – fornece subsídios para a Netflix optar para quais públicos (faixas etárias) investirá mais fortemente.

5)	Países com mais produções por Gênero – agrupamento de países por gênero. Permite a resposta a seguintes questões: qual o país que produz mais comédias? Esta informação é relevante para a Netflix tomar sobre qual gênero investir em um determinado país.

6)	Qual o tipo de conteúdo mais lançado pela Netflix, filmes ou séries e o percentual de cada um?

7)	É possível responder às seguintes métricas de desempenho:

  a.	Top 10 diretores – ranking de diretores que mais lançaram conteúdo.
  
  b.	Top 10 atores – ranking de diretores que mais atuaram;
  
  c.	Top 10 gêneros – quais são os gêneros mais populares;
  
  d.	Top 10 países – quais países possuem mais lançamentos.

