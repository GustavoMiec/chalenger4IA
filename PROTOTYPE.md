# Demonstração do Protótipo Funcional

O código apresentado implementa um protótipo funcional de um sistema de análise de sentimentos que utiliza técnicas de Processamento de Linguagem Natural (PLN) para classificar tweets em emoções positivas e negativas. O sistema é desenvolvido em Python, utilizando bibliotecas populares como pandas, scikit-learn, nltk e wordcloud. Aqui estão os principais componentes e funcionalidades:

## Principais Componentes e Funcionalidades

- **Carregamento de Dados**: Os dados são carregados de um arquivo CSV contendo tweets e suas respectivas classificações de sentimentos.

### Pré-processamento de Dados:
- **Remoção de Nulos**: Linhas com valores nulos são removidas do conjunto de dados.
- **Tokenização**: O texto dos tweets é tokenizado utilizando diferentes métodos (tokenização por espaços em branco e pontuação).
- **Remoção de Stopwords**: Palavras irrelevantes (stopwords) e pontuação são removidas para melhorar a qualidade da análise.
- **Stemming**: O processo de stemming é aplicado para reduzir palavras a suas raízes.

### Visualização de Dados:
- São geradas nuvens de palavras para visualizar a frequência de palavras nos tweets positivos e negativos, além de gráficos de Pareto para identificar as palavras mais frequentes.

### Vetorizações:
- O texto é vetorizado utilizando CountVectorizer e TfidfVectorizer para converter os tweets em uma forma numérica que pode ser utilizada para treinamento de modelos.

### Classificação:
- Um modelo de Regressão Logística é treinado para classificar os tweets com base nas características extraídas. A acurácia do modelo é calculada para diferentes tratamentos de pré-processamento.

### Interatividade:
- Um protótipo de interface em HTML permite ao usuário digitar uma frase e prever a emoção associada a ela com base em palavras-chave.

# Análise Detalhada da Arquitetura de IA

## 1. Arquitetura Geral
O sistema é estruturado em módulos, cada um responsável por uma tarefa específica:
- Carregamento e pré-processamento de dados.
- Análise exploratória e visualização.
- Extração de características.
- Treinamento e avaliação do modelo.
- Interação com o usuário através de uma interface web.

## 2. Processamento de Linguagem Natural (PLN)
- **Tokenização**: Utiliza diferentes estratégias de tokenização para lidar com a diversidade do texto em português.
- **Remoção de Stopwords**: O uso de stopwords personalizadas é crucial para a eliminação de palavras que não contribuem para a análise de sentimentos.
- **Stemming**: A aplicação do stemmer RSLP é uma escolha apropriada para o idioma português, pois reduz palavras a suas raízes.

## 3. Extração de Características
- **Bag of Words e TF-IDF**: Ambas as técnicas são utilizadas para transformar texto em representações numéricas. O TF-IDF é particularmente eficaz para medir a relevância de palavras em relação ao corpus, considerando a frequência de cada palavra em um documento em relação à sua frequência geral.

## 4. Modelo de Classificação
- **Regressão Logística**: Escolhida por sua simplicidade e eficácia em problemas de classificação binária, a regressão logística é aplicada nos dados vetorizados. A acurácia é avaliada para diferentes conjuntos de dados, permitindo comparar a eficácia de cada tratamento.

## 5. Interface do Usuário
- **HTML e JavaScript**: Uma interface básica é criada para interação com o usuário, permitindo a entrada de frases e retornando a previsão de sentimentos. A lógica de previsão é baseada em palavras-chave, proporcionando uma experiência interativa.

# Implementação
A implementação do código segue as melhores práticas de programação, incluindo:
- **Modularização**: Funções bem definidas para cada etapa do processamento de dados e análise.
- **Comentários**: Uso de comentários para descrever a finalidade de cada bloco de código.
- **Visualização**: Gráficos e nuvens de palavras são utilizados para proporcionar insights sobre os dados.

# Conclusão
O protótipo demonstrado é uma solução eficaz para a análise de sentimentos em tweets, utilizando técnicas de PLN e aprendizado de máquina. A arquitetura e a implementação são bem estruturadas, permitindo fácil manutenção e expansão futura do sistema.
