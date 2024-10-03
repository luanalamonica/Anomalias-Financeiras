# Detecção de Anomalias em Transações Financeiras (Power BI + R)

Este projeto foi desenvolvido durante o curso "Microsoft Power BI Para Business Intelligence e Data Science" da Data Science Academy (DSA). O objetivo do projeto é criar um Dashboard no Power BI que realiza a detecção de anomalias em transações financeiras, utilizando a Linguagem R para análise e visualização de dados.

## Funcionalidades

- **Detecção de Anomalias**: O sistema identifica anomalias em um conjunto de dados de transações financeiras, utilizando algoritmos implementados em R.
- **Visualização Interativa**: O Power BI é utilizado para construir dashboards interativos, permitindo que os usuários visualizem as anomalias detectadas em gráficos intuitivos.
- **Integração com R**: O projeto faz uso da integração entre Power BI e R para realizar a análise estatística e detectar comportamentos fora do padrão.

## Tecnologias Utilizadas

- **Power BI**: Para construção do dashboard e visualização de dados.
- **Linguagem R**: Para análise de dados e detecção de anomalias nas transações financeiras.
- **RStudio**: Ambiente de desenvolvimento integrado (IDE) utilizado para escrever o código em R.

## Pré-requisitos

Antes de executar este projeto, certifique-se de ter instalado:

- [Power BI Desktop](https://powerbi.microsoft.com/pt-br/desktop/)
- [R](https://www.r-project.org/) (versão 3.6 ou superior)
- [RStudio](https://rstudio.com/products/rstudio/download/) (opcional, para editar e rodar scripts R)
- [Pacotes R](https://cran.r-project.org/web/packages/available_packages_by_name.html) necessários para detecção de anomalias, como `forecast`, `anomalize`, `ggplot2`, entre outros.

## Instruções para Execução

### 1. Criando o Gráfico com R

A primeira etapa do projeto é a criação do código em R para detectar anomalias nos dados financeiros. Isso foi feito no RStudio, onde foram carregados os dados, aplicados os algoritmos de detecção e gerados os gráficos necessários.

![Criando o gráfico na Linguagem R](https://github.com/luanalamonica/Anomalias-Financeiras/blob/main/R%20studio.png?raw=true)

#### Código Exemplo em R

```r
# Instalação de pacotes necessários
install.packages("anomalize")
install.packages("ggplot2")
install.packages("dplyr")

# Carregando pacotes
library(anomalize)
library(ggplot2)
library(dplyr)

# Exemplo de código para detectar anomalias
dados <- read.csv("transacoes_financeiras.csv")

# Aplicando a detecção de anomalias
resultado <- dados %>%
    time_decompose(valor_transacao) %>%
    anomalize(remainder) %>%
    time_recompose()

# Plotando os resultados
plot_anomalies(resultado)
