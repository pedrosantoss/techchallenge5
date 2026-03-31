# TECH CHALLENGE - FASE 05

---

# Análise de Reclamações Bancárias com NLP e Deep Learning

## Visão Geral
Este projeto tem como objetivo analisar reclamações de clientes do setor bancário por meio de técnicas de **Processamento de Linguagem Natural (NLP)** e **Deep Learning**. A partir dos textos das reclamações, são realizadas análises de sentimento, identificação de padrões e mapeamento dos principais temas de insatisfação, com foco em apoiar diagnósticos estratégicos para instituições financeiras.

---

## Objetivo do Trabalho
- Realizar análise de sentimento das reclamações bancárias  
- Treinar um modelo de classificação utilizando Deep Learning  
- Identificar e agrupar os principais temas recorrentes

---

## Base de Dados
O estudo utiliza um dataset de reclamações bancárias em formato CSV, contendo descrições textuais dos relatos dos clientes. Para fins de desempenho e balanceamento, foi utilizada uma amostra aleatória das reclamações, além da criação de comentários positivos únicos.

---

## Tecnologias Utilizadas
- Python  
- Pandas e NumPy  
- NLTK  
- Scikit-learn  
- TensorFlow / Keras  
- Transformers (Hugging Face – DistilBERT)  
- Matplotlib, Seaborn e WordCloud  

---

## Metodologia

### Pré-processamento de Texto
Os dados passaram por etapas de limpeza e normalização, incluindo:
- Conversão para letras minúsculas  
- Remoção de caracteres repetidos e ruídos  
- Tokenização  
- Remoção de stopwords  
- Lematização utilizando POS tagging  

O resultado foi armazenado em uma nova coluna contendo o texto limpo.

---

### Análise de Sentimento
Foi aplicada uma abordagem baseada em um modelo pré-treinado **DistilBERT**, utilizado para classificar as reclamações em sentimento **positivo** ou **negativo**. O processamento ocorreu em lotes para suportar textos longos, e o sentimento final foi definido com base na maior probabilidade prevista pelo modelo.

---

### Balanceamento do Dataset
Devido ao desbalanceamento entre as classes de sentimento, foi adotada uma estratégia de balanceamento dinâmico, com geração sintética de textos positivos, mantendo uma proporção controlada entre as classes para melhorar o desempenho dos modelos supervisionados.

---

### Vetorização e Modelagem Supervisionada
Os textos foram vetorizados utilizando **TF-IDF**. Em seguida, foi treinado um modelo de **Rede Neural Artificial** com Keras, utilizando camadas densas e dropout para regularização. O conjunto de dados foi dividido em treino e teste de forma estratificada.

---

### Avaliação do Modelo
O desempenho do modelo foi avaliado utilizando as seguintes métricas:
- Accuracy  
- Precision  
- Recall  
- F1-score  
- AUC-ROC  

Os resultados indicaram alto desempenho preditivo, com excelente capacidade de diferenciação entre sentimentos positivos e negativos.

---

### Clusterização e Identificação de Temas
Para identificar os principais temas das reclamações, foi aplicado o algoritmo **KMeans** sobre a matriz TF-IDF. A partir dos clusters gerados, foram extraídas palavras-chave representativas, permitindo a associação dos grupos a temas como:
- Conta corrente e cartões  
- Pagamentos e empréstimos atrasados  
- Fraude e roubo de identidade  
- Cobrança de dívidas  
- Relatórios de crédito e disputas  

---

### Análise das Dores dos Clientes
Foram utilizadas técnicas de visualização, como **word clouds** e gráficos de frequência, para identificar os termos mais recorrentes e os temas que concentram maior volume de reclamações, possibilitando uma visão clara das principais causas de insatisfação dos clientes.

---

## Principais Resultados
- Predominância de sentimento negativo nas reclamações analisadas  
- Alta recorrência de temas relacionados a atraso de pagamentos e fraude  
- Eficiência do uso combinado de BERT, TF-IDF e Redes Neurais  
- Modelo supervisionado com desempenho elevado  

---

## Conclusão
O projeto demonstra o potencial do uso de técnicas de NLP e Deep Learning para análise de reclamações bancárias em larga escala. A abordagem adotada permite transformar dados textuais não estruturados em informações estratégicas, auxiliando instituições financeiras na identificação de falhas operacionais e na melhoria da experiência do cliente.
