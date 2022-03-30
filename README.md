# Predição de faturamento usando séries temporais
------------------
## Introdução
Meu segundo projeto de machine learning onde uso os conceitos de séries temporais para prever o faturamento de vendas de uma empresa para um período de 14 meses. Nesse projeto temos um dataset com as vendas mês a mês de 5 produtos de vendas B2B e a proposta é prever o faturamento usando os valores totais de faturamento mês a mês e comparar com a predição realizada a partir da soma das predições individuais de cada produto.

5 produtos que são comercializados pela empresa:
- Produtos alimentícios
- Auxilio de final de ano
- Saúde
- Bonificação
- Transporte


## Desenvolvimento

Esse projeto foi dividido em 4 grandes etapas:

1) Análise exploratória dos dados (EDA)
2) Predição do faturamento mês a mês para os próximos 14 meses usando um modelo de série temporal a partir do faturamento total mês a mês
3) Predição do faturamento mês a mês para os próximos 14 meses usando a soma das predições dos modelos de série temporal de cada produto a partir do faturamento total mês a mês dos mesmos
4) Conclusões sobre o uso de cada um dos modelos e conclusão geral



## Conclusão

A previsão do total de vendas para os próximos 14 meses usando a soma de cada previsão dos produto apresentou um comportamento próximo ao estimado usando somente a série do faturamento total mês a mês. É perceptível que a modelo usando o faturamento total mês a mês parece ter capturado melhor o comportamento da curva dos valores já existentem. Isso acontece em grande parte porque nas séries de saúde, bonificação e transporte foi encontrado um modelo ótimo que poderia ser bastante otimizado com técnicas que deixariam a série mais estacionaria (média móvel, log, exp, dentre outras). No entanto, como o ajuste da serie de produto alimentício (maior relevância) foi efetivo, os efeitos dos outros produtos não prejudicam tanto a previsão do faturamento total.

Considerando que o problema acima fosse em uma empresa real, seria mais efetivo prever o faturamento total usando cada produto individualmente, já que são somente 5 produtos e é possível otimizar o modelo para cada produto sem tanto gasto de tempo. Caso o volume de produtos fosse maior (15,20 produtos) seria mais prudente prever o faturamento total com base no valor de vendas mês a mês dos produtos de maior relevância já que o gasto de tempo com a modelagem seria extenso e a modelagem ótima de produtos com baixa representatividade no faturamento não alteraria o valor final de forma significativa.

