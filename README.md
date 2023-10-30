# Teste A/B para jogos de celular

## Visão Geral

O conjunto de dados que temos são de 90.189 jogadores que instalaram o jogo Cookie Cats enquanto o teste A/B estava em execução.

Você pode conferir o dataset e o projeto na íntegra clicando abaixo:

Link dataset: https://www.kaggle.com/datasets/mursideyarkin/mobile-games-ab-testing-cookie-cats/data

Link do código do projeto: https://github.com/gustavoptavares/Teste-A-B-Jogos-de-Celular/blob/main/Teste_A_B_Jogos_de_Celular.ipynb

## Problema e Solução

Vamos analisar os dados o conjunto de dados de 90.189 jogadores. Cookie Cats é um jogo móvel extremamente popular desenvolvido pela Tactile Entertainment, vamos entender, no detalhe, aspectos relacionados as mudanças de versões dos jogos, como:

• Enteder o conjunto de dados e o impacto nas mudanças.

• Fazer teste A/B para avaliar se há uma diferença significativa na retenção de jogadores entre as duas versões do jogo.

## O Processo

O primeiro passo do projeto foi adquirir os dados. Utilizamos os dados do portal Kaagle, carregando-o no Google Colab, para a exploração e análise dos dados utilizando a linguagem de programação Python e suas bibliotecas, como Pandas, Matplotlib e Scipy. Neste projeto foi feito, uma análise exploratória, e foi feito testes estatísticos para avaliar o impacto da mudança das versões dos jogos na retenção de jogadores.

## Resultados

Resultados do Teste A/B

Distribuição da Métrica de Retenção: A análise das distribuições de retenção para cada grupo (versões gate_30 e gate_40) é realizada, possivelmente incluindo a visualização dessas distribuições.

Normalidade das Distribuições: Um teste de normalidade (como o teste Shapiro-Wilk) é aplicado para verificar a normalidade das distribuições de retenção nos grupos. Se o p-valor é menor que um limiar (geralmente 0,05), a hipótese de normalidade é rejeitada, indicando que a distribuição dos dados não é normal. Se o p-valor é maior, não rejeitamos a hipótese de normalidade. O resultado do P-valor para o teste de normalidade no gate_30: 6.35628983417737e-42. O resultado do P-valor para o teste de normalidade no gate_40: 1.1211789013062861e-41.

Teste t de Student: Um teste t de Student é realizado para comparar as médias de retenção entre gate_30 e gate_40. O resultado deste teste é expresso através de um P-valor para o teste t: 0.07441111525563184

Inferência Estatística: Se o P-valor para o teste t for menor que um limiar estabelecido (geralmente 0,05), a hipótese nula é rejeitada, indicando uma diferença estatisticamente significativa na retenção entre as versões do jogo. Caso contrário, não há evidências suficientes para rejeitar a hipótese nula, sugerindo que as mudanças entre as versões não têm impacto significativo na retenção.

Recomendação: Não rejeitamos a hipótese nula (H0). A mudança não tem efeito significativo na retenção de jogadores. Recomenda-se não implementar a mudança, pois ela não apresentou impacto significativo na retenção de jogadores.

## Conclusões

A conclusão do teste A/B depende do valor-p obtido e do limiar de significância estabelecido. Se o teste encontrou uma diferença significativa, isso indica que uma das versões do jogo é superior em termos de retenção de jogadores. Se não houver diferença significativa, isso sugere que as alterações entre as versões do jogo não influenciam a retenção dos jogadores de maneira perceptível.

A recomendação final, se basear na implementação de mudanças no jogo, deve considerar os resultados do teste A/B juntamente com outras métricas e considerações de negócios. Por exemplo, se uma versão do jogo melhorar a retenção, mas for mais cara ou mais difícil de manter, esses fatores também devem ser levados em conta.
