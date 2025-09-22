
# 🧠 Sistematização - Insurance Cost Prediction

Esse projeto em machine learning visa prever valores de custo de seguro médico com base no IMC, gênero, região, status de tabagismo, número de crianças e idade.

## 🖥 Acesse Online o Dataset

👉 [Clique Aqui](https://www.kaggle.com/datasets/mosapabdelghany/medical-insurance-cost-dataset/data) para visualizar o dataset no Kaggle.


## 🚀 Como reproduzir o projeto?

O modelo foi desenvolvido em notebook no Google Colab. O notebook "Codigo_Fonte_Sistematizacao_CD_II.ipynb" contém o seguinte conteúdo:
- Download do dataset via API do Kaggle
- Análise exploratória (EDA)
- Pré-processamento
- Treinamento dos modelos
- Avaliação (R² e MAE)
- Teste com dataset aleatório

Se não quiser utilizar o notebook pronto, criar um novo notebook no Google Colab e seguir o mesmo passo a passo:

1. 
 ```bash
   git clone https://github.com/laryssabueno/Sistematizacao-Insurance-Prediction.git
   cd Sistematizacao-Insurance-Prediction
```
2. Configure a API do Kaggle:

- Baixe sua chave em: Kaggle Account Settings > API > Create New Token
- Deve gerar um arquivo kaggle.json, caso tenha outro nome, renomear.
- No Google Colab, faça upload do arquivo conforme mostrado no notebook.

3. No Google Colab, faça o upload do kaggle e faça o seguinte:
```
!pip install kaggle

# Subir o arquivo kaggle.json (chave da API baixada no site do Kaggle)
from google.colab import files
files.upload()  # subir kaggle.json

# Criar pasta e mover credencial
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json

# Baixar dataset
!kaggle datasets download -d mosapabdelghany/medical-insurance-cost-dataset -p ./data --unzip
```
4. Instale as dependências:
```
pip install -r requirements.txt
```

5. Importar arquivos de modelos e encoder para o google colab (se encontram na pasta models/).

```
enconder = joblib.load('encoder.joblib')
model_lr = joblib.load('model_linearregression.pkl')
model_rr = joblib.load('model_randomforestregressor.pkl')
```
## ✅ Resultados

- R2 Score (LinearRegression): 72.70 %
- R2 Score (RandomForestRegressor): 82.92 %
- Mean Absolute Error (LinearRegression): 4301.793232211164
- Mean Absolute Error (RandomForestRegressor): 2505.125493548589
- Mean Absolute Percentage Error (LinearRegression): 52.85 %
- Mean Absolute Percentage Error (RandomForestRegressor): 31.26 %


## 🤔 Aprendizados

A atividade conseguiu induzir pensamentos de um cientista de dados:
- Analisar e entender o dataset
- Trabalhar as variáveis para se adequarem melhor ao problema proposto
- Pipeline do projeto preditivo - qual melhor se adequa aos dados e problema proposto
- Analise de resultados
- Teste de modelagem


![Logo](https://institucional.uniceub.br/hubfs/BrandCenter/img/logo-ceub-assinatura-conceito-centralizado-01.png)

