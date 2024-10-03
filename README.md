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

```

### 2. Criando o Dashboard no Power BI

Com os gráficos e dados processados no R, a segunda etapa foi a criação de um dashboard interativo no Power BI. O Power BI foi configurado para importar os resultados da análise em R e exibir as anomalias detectadas de maneira visual e interativa.

![Dashboard criado no Power BI](https://github.com/luanalamonica/Anomalias-Financeiras/blob/main/dashboard%20R.png?raw=true)

#### Passos para Importar o Script R no Power BI:

1. Abra o **Power BI Desktop**.
2. Vá até a aba **Visualizações** e selecione **Visual R Script**.
3. Copie e cole o código R no editor de script do Power BI.
4. Execute o script e visualize o gráfico gerado diretamente no painel do Power BI.
5. Personalize o dashboard para incluir filtros e gráficos adicionais.

## Como Executar o Projeto

1. Clone este repositório:
    ```bash
    git clone https://github.com/luanalamonica/Anomalias-Financeiras.git
    ```

2. Abra o código R no RStudio e execute o script para gerar os dados e gráficos.

3. No Power BI, importe o script R gerado e configure os gráficos interativos no dashboard.

4. Explore o dashboard para visualizar as anomalias nas transações financeiras.

## Estrutura do Projeto

- **RStudio Scripts**: Contém os scripts R usados para processar os dados e detectar anomalias.
- **Dashboard Power BI**: Dashboard interativo criado no Power BI, utilizando gráficos gerados pelo script R.

## Melhorias Futuras

- Implementar novos algoritmos de detecção de anomalias para melhorar a precisão.
- Adicionar mais fontes de dados e variáveis para refinar as análises.
- Incluir uma camada de automação, para que o sistema realize a detecção de anomalias em tempo real.
- Incorporar alertas automáticos no Power BI para notificar sobre novas anomalias.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para adicionar novas funcionalidades, melhorar o código ou ajustar o dashboard. Para contribuir:

1. Faça um _fork_ deste repositório.
2. Crie uma _branch_ com a nova funcionalidade (`git checkout -b feature/nova-funcionalidade`).
3. Envie suas alterações para o repositório (`git push origin feature/nova-funcionalidade`).
4. Abra um _pull request_ para revisão.
