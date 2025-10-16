# 🚕 Análise de Dados de Corridas de Táxi em Chicago 📊

---

## 📝 Descrição do Projeto

Este projeto consiste em uma análise exploratória de dados e um teste de hipótese estatística relacionados a serviços de táxi na cidade de **Chicago**. O objetivo principal é analisar o volume de viagens por empresa e por bairro de destino, além de investigar se as **condições climáticas ruins afetam a duração das viagens** entre a Loop Central e o Aeroporto O'Hare (ORD).

Os dados utilizados foram previamente coletados a partir de consultas SQL e estão divididos em três arquivos CSV.

---

## 🎯 Objetivos da Análise

1.  **Exploração de Dados:** Entender a estrutura e a qualidade dos três conjuntos de dados fornecidos (`trips_by_company`, `dropoff_stats`, `loop_to_ohare`).
2.  **Ranking de Empresas e Bairros:** Identificar as **10 principais empresas de táxi** por número de viagens e os **10 bairros com mais destinos (drop-offs)**.
3.  **Visualização:** Gerar gráficos para exibir os rankings identificados.
4.  **Teste de Hipótese:** Realizar um teste t de Student para verificar a seguinte hipótese estatística:
    > "A duração média das viagens do Loop ao Aeroporto O'Hare é diferente em dias de condições climáticas ruins em comparação com dias de boas condições climáticas."

---

## 🛠️ Tecnologias e Bibliotecas

O projeto foi desenvolvido em **Python** utilizando o ambiente Jupyter Notebook. As seguintes bibliotecas foram empregadas:

* **`pandas`**: Para manipulação e análise dos dados em DataFrames.
* **`matplotlib.pyplot`**: Para a criação de visualizações estáticas.
* **`seaborn`**: Para visualizações estatísticas atrativas.
* **`scipy.stats` (ttest_ind)**: Para a realização do teste de hipótese t de Student.

---

## 📂 Estrutura dos Dados

Foram utilizados três conjuntos de dados, provenientes de consultas SQL pré-executadas. A estrutura de cada um é a seguinte:

| Arquivo | Descrição | Colunas Principais |
| :--- | :--- | :--- |
| `project_sql_result_01.csv` | Total de viagens por empresa de táxi. | `company_name` (string), `trips_amount` (int) |
| `project_sql_result_04.csv` | Média de viagens de táxi para cada bairro de destino (dropoff) em novembro de 2017. | `dropoff_location_name` (string), `average_trips` (float) |
| `project_sql_result_07.csv` | Dados de viagens entre a Loop Central e o Aeroporto O'Hare (ORD) em novembro de 2017. | `start_ts` (timestamp), `weather_conditions` (string), `duration_seconds` (float) |

---

## ⚙️ Como Executar o Projeto

### Pré-requisitos

Certifique-se de ter o **Python** (versão 3.x) instalado, juntamente com as bibliotecas necessárias.

### Instalação das Dependências

Você pode instalar as bibliotecas necessárias usando `pip`:

```bash
pip install pandas matplotlib seaborn scipy jupyter
````
---

### Execução

Baixe ou clone este repositório.

Certifique-se de que os arquivos de dados (project_sql_result_01.csv, project_sql_result_04.csv, project_sql_result_07.csv) estão disponíveis no caminho de dados especificado no notebook (/datasets/).

Abra o Jupyter Notebook ou JupyterLab e navegue até o arquivo do projeto.

Execute as células do notebook em sequência para carregar os dados, realizar a análise exploratória, gerar as visualizações e executar o teste de hipótese.

---

### 📈 Resultados Principais (Visão Geral)

Empresa Mais Popular: A empresa Flash Cab lidera o número de viagens.

Destino Mais Popular: A área de Loop é o bairro de destino com a maior média de viagens.

Resultado do Teste de Hipótese: A análise estatística indicará se a duração média das viagens é significativamente maior quando as condições climáticas são ruins, ou se a diferença observada pode ser atribuída apenas ao acaso. (O resultado exato está detalhado no final do notebook).

---

🤝 Contato
Para dúvidas ou sugestões, entre em contato:

**joice_fsouza@hotmail.com**
