# Desafio Ciência de Dados - Lighthouse 2024

Este repositório contém a solução para o Desafio de Ciência de Dados da Lighthouse, 2024. O objetivo do desafio é analisar um banco de dados cinematográfico e orientar qual tipo de filme deve ser desenvolvido, além de prever a nota do IMDB para filmes.

## Estrutura do Projeto

- `notebooks/`
  - `EDA_and_analysis.ipynb`: Análise exploratória dos dados e respostas às perguntas do desafio.
  - `modeling_and_prediction.ipynb`: Códigos de modelagem e previsão da nota do IMDB.
- `data/`
  - `desafio_indicium_imdb.csv`: Base de dados utilizada (você precisa substituir com seu arquivo real).
- `models/`
  - `imdb_rating_model.pkl`: Modelo treinado salvo.
- `requirements.txt`: Lista de pacotes necessários para executar o projeto.
- `README.md`: Este arquivo com instruções de instalação e execução.

## Instalação

Para executar o projeto localmente, siga os passos abaixo:

1. **Clone o repositório:**

   ```bash
   git clone https://github.com/seu-usuario/lh_cd_seunome.git
   cd lh_cd_seunome
   ```

2. **Crie um ambiente virtual:**

   ```bash
   python -m venv venv
   ```

3. **Ative o ambiente virtual:**

   - No Windows:
     ```bash
     venv\Scripts\activate
     ```
   - No macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

4. **Instale as dependências:**

   ```bash
   pip install -r requirements.txt
   ```

## Execução

### Análise Exploratória e Respostas às Perguntas

1. Navegue até a pasta `notebooks` e abra o Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

2. Abra e execute o notebook `EDA_and_analysis.ipynb` para visualizar a análise exploratória dos dados e as respostas às perguntas do desafio.

### Modelagem e Previsão

1. Navegue até a pasta `notebooks` e abra o Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

2. Abra e execute o notebook `modeling_and_prediction.ipynb` para visualizar o código de modelagem e prever a nota do IMDB para filmes.

### Previsão para um Filme Específico

Para prever a nota do IMDB para um filme específico, utilize o modelo salvo (`imdb_rating_model.pkl`). Exemplo de uso no Python:

```python
import numpy as np
import pickle

# Características do filme "The Shawshank Redemption"
shawshank_features = np.array([[1994, 80.0, 2343110]])

# Carregar o modelo salvo
with open('models/imdb_rating_model.pkl', 'rb') as f:
    loaded_model = pickle.load(f)

# Fazer a previsão
shawshank_rating_pred = loaded_model.predict(shawshank_features)
print(f"A nota prevista para o filme 'The Shawshank Redemption' é: {shawshank_rating_pred[0]}")
```
