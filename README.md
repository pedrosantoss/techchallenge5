# TechChallenge 5: Análise de Sentimentos com Deep Learning

Este é um projeto de Análise de Sentimentos com a utilização DistilBERT e Deep Learning idealizado na linguagem Python, versão 3.12.

No projeto foram realizados o processamento e a análise de sentimentos de um conjunto de dados de comentários de clientes de uma instituição financeira, o dataset analisado foi extraído em: https://www.kaggle.com/api/v1/datasets/download/shashwatwork/consume-complaints-dataset-fo-nlp

O objetivo principal do projeto é classificar se um comentário é negativo (0) ou positivo (1). 

As seguintes bibliotecas foram utilizadas:
Manipulação de dados: pandas, numpy
Limpeza e pré-processamento: nltk (Tokenização, Stopwords, Lemmatização com POS Tagging)
NLP (Processamento de Linguagem Natural): nltk (Tokenização, Stopwords, Lemmatização com POS Tagging)
Classificação de Sentimento: transformers (Hugging Face) utilizando o modelo DistilBERT (distilbert-base-uncased-finetuned-sst-2-english)
Vetorização: Scikit-learn (TF-IDF Vectorizer)
Deep Learning: TensorFlow / Keras (Rede Neural Densa)
Visualização: matplotlib, seaborn, wordcloud

O projeto foi estrturado da seguinte maneira:
1. Pré-processamento de Texto
2. Rotulagem com DistilBERT
3. Balanceamento de Dados
4. Vetorização (TF-IDF) e aplicação do Modelo de Deep Learning (Keras)
5. Análise Visual


Resultados:
O projeto entrega um modelo capaz de prever, confiavelmente, o sentimento de um comentário e wordclouds e gráficos (gerados baseados em clusterização) sobre as dores dos clientes. 
