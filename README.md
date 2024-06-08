### Exemplo Prático de uma Rede Neural com Keras e TensorFlow

Neste exemplo prático, vamos construir e treinar uma rede neural simples para classificar imagens de dígitos manuscritos usando o conjunto de dados MNIST. O MNIST é um dos conjuntos de dados mais utilizados em aprendizado de máquina e visão computacional, composto por imagens de dígitos manuscritos (0 a 9).

#### Passos do Exemplo:

1. **Importar Bibliotecas Necessárias:**
   Primeiro, importamos as bibliotecas necessárias, incluindo TensorFlow e Keras para construção e treinamento da rede neural, e Matplotlib para visualização das imagens.

2. **Carregar e Preparar os Dados:**
   Carregamos o conjunto de dados MNIST, que contém 60.000 imagens de treinamento e 10.000 imagens de teste. As imagens são normalizadas para que os valores dos pixels estejam entre 0 e 1. Além disso, os rótulos são convertidos para o formato one-hot, necessário para a saída da rede neural.

3. **Construir o Modelo da Rede Neural:**
   Construímos um modelo sequencial de rede neural. Este modelo inclui:
   - Uma camada de achatamento (`Flatten`) que transforma as imagens de 28x28 pixels em vetores de 784 elementos.
   - Uma camada densa (`Dense`) oculta com 128 neurônios e função de ativação ReLU.
   - Uma camada de saída (`Dense`) com 10 neurônios (um para cada dígito) e função de ativação softmax.

4. **Compilar o Modelo:**
   Compilamos o modelo especificando o otimizador Adam, a função de perda de entropia cruzada categórica e a métrica de precisão. A função de perda ajuda o modelo a medir o quão bem ele está fazendo durante o treinamento, enquanto a métrica de precisão nos dá uma ideia de quão bem o modelo está performando.

5. **Treinar o Modelo:**
   Treinamos o modelo com 5 épocas, usando um tamanho de lote de 32. Durante o treinamento, também validamos o modelo com o conjunto de dados de teste para monitorar a performance e evitar overfitting.

6. **Avaliar o Modelo:**
   Após o treinamento, avaliamos a precisão do modelo no conjunto de dados de teste. Isso nos dá uma ideia de quão bem o modelo generaliza para novos dados.

7. **Fazer Previsões:**
   Usamos o modelo treinado para prever os rótulos das imagens de teste. Em seguida, visualizamos algumas dessas imagens junto com suas previsões e rótulos verdadeiros, para verificar a performance do modelo.

#### Visualização das Imagens:
Para uma melhor compreensão dos resultados, exibimos algumas imagens de teste com suas respectivas previsões feitas pelo modelo. Isso nos permite ver onde o modelo acertou e onde errou, ajudando na análise qualitativa da performance do modelo.

Este exemplo prático demonstra os passos essenciais para construir, treinar e avaliar uma rede neural simples utilizando Keras e TensorFlow, fornecendo uma base sólida para tarefas de classificação de imagens.
