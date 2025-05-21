# 🧠 Processamento de Linguagem Natural em Português 🇧🇷

Este notebook demonstra técnicas fundamentais de **Processamento de Linguagem Natural (PLN)** com foco no idioma **português**, utilizando bibliotecas como **NLTK**, **spaCy** e **Transformers**. São abordadas tarefas como tokenização, remoção de stopwords, análise sintática, semântica e análise de sentimentos.

---

## 🔧 Requisitos

- Python 3.x  
- Bibliotecas:
  - `nltk`
  - `spacy`
  - `transformers`
  - `torch`  
- Modelos spaCy:
  - `pt_core_news_sm`
  - `pt_core_news_lg` (opcional para análise semântica)
  - `en_core_web_sm` (para exemplos em inglês)

---

## 📚 Conteúdo do Notebook

### 1. 🧩 Tokenização e Remoção de Stopwords
- Quebra do texto em tokens (palavras).
- Remoção de palavras comuns (stopwords) e pontuação com `nltk`.

### 2. 🔤 Lematização e Stemização
- **Stemização** com `RSLPStemmer` (NLTK).
- **Lematização** com `spaCy`, usando modelos treinados em português.

### 3. 🧠 Análise Morfológica e Sintática
- Identificação da classe gramatical (POS tagging).
- Análise sintática e estrutura frasal (dependency parsing).
- Utilização do modelo `pt_core_news_sm` com `spaCy`.

### 4. 🧾 Reconhecimento de Entidades Nomeadas (NER)
- Extração de entidades como pessoas, locais, organizações, datas, etc.
- Comparação entre modelos em português e inglês.

### 5. 🧠 Análise Semântica
- Cálculo de similaridade semântica entre frases.
- Exemplo: "Eu comprei um carro" vs "Adquiri um automóvel".
- Requer `pt_core_news_lg`, modelo com vetores semânticos.

### 6. 😊 Análise de Sentimentos
- Classificação de frases em **positivas**, **negativas** ou **neutras**.
- Utiliza o modelo multilingue `nlptown/bert-base-multilingual-uncased-sentiment` da Hugging Face com `transformers`.

---

## 🗂 Exemplos de Uso

```python
# Análise de sentimentos
from transformers import pipeline

analisador = pipeline("sentiment-analysis", model="nlptown/bert-base-multilingual-uncased-sentiment")
print(analisador("Este filme foi maravilhoso!"))
```

## [Link Para o Notebook no Google Colab](https://colab.research.google.com/drive/1aM1ylbAvEgRZ2IrQ-qHfwXPrcTccYcur#scrollTo=e0zcjs6ZPpTu)

## 📌 Observações
Alguns modelos podem ser lentos para baixar na primeira execução.

O modelo pequeno do spaCy (pt_core_news_sm) não calcula similaridade semântica corretamente.

Para melhores resultados em semântica, utilize o modelo pt_core_news_lg.

## 📎 Referências
NLTK Documentation

spaCy Documentation

Hugging Face Transformers

## 🚀 Autor
Este notebook foi desenvolvido como parte de estudos e experimentos com técnicas de PLN aplicadas ao idioma português.
Sinta-se à vontade para contribuir ou abrir issues!
