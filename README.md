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
