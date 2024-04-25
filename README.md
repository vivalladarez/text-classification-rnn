# MVP - Machine Learning & Analytics 🤖📊

Este projeto corresponde ao MVP da terceira sprint do curso de Pós-Graduação em Ciência de Dados e Analytics da PUC-Rio.

## Problemática
O objetivo deste trabalho é construir um classificador de sentimentos utilizando um modelo de Deep Learning baseado em redes neurais recorrentes (RNN), com dados provenientes de avaliações de aplicativos disponíveis na Google Play Store. Isso fornecerá insights valiosos para os desenvolvedores e empresas sobre a percepção de seus produtos pelos usuários.

## Dataset
Utilizou-se o dataset "App Reviews", contendo análises dos usuários nos aplicativos da Google Play Store. Para cada avaliação textual, é atribuída uma classificação numérica de 1 a 5, refletindo o nível de satisfação dos usuários com o aplicativo.

**Atributos Utilizados:**

`content`: Descritivo da avaliação do usuário para o aplicativo

`score`: Nota dado pelo avaliador de 0 a 5 para o aplicativo

**Coleta de Dados:**

Foram extraídas informações dos principais aplicativos de comida/entrega, incluindo:
- iFood
- Rappi
- Uber
- Eats
- McDonald's
- Burger King
- Aiqfome.

## Análise e Pré-processamento do Dataset
- Análise dos Dados: Investigou-se a distribuição das amostras por score e padrões específicos associados a cada uma delas.
- Limpeza dos Dados: Realizou-se a remoção de informações ruidosas, unificando os dados e reduzimos as classes para duas: 0 (sentimentos negativos) ou 1 (sentimentos positivos).
- Treino e Teste: Dividiu-se os dados em conjuntos de treinamento e teste, foi empregado a validação cruzada e o processo de TextVectorization.

## Criação do Modelo
Explorou-se diferentes parâmetros e arquiteturas de rede neural recorrente (RNN)
- Avaliação de Hiperparâmetros
- Recurrent Neural Network (RNN) - Uma camada LSTM
- Recurrent Neural Network (RNN) - Empilhamento de duas camadas LSTM

## Resultados e Conclusões
O modelo empilhado com duas camadas LSTM demonstrou uma capacidade mais robusta de aprender e generalizar padrões nos dados, superando o modelo de uma camada LSTM. A análise dos gráficos de Accuracy e Loss indicou que o modelo empilhado convergiu de maneira mais estável, enquanto o modelo de uma camada LSTM mostrou sinais de possível overfitting. Portanto, concluímos que o modelo empilhado com duas camadas LSTM é mais adequado para a tarefa de análise de sentimentos em avaliações de aplicativos de comida/entrega.
